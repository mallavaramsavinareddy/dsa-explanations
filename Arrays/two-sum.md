# Two Sum Problem in leetcode

## Problem
Given an array of integers and a target, return indices of two numbers that add up to target.

##  Approach
We use a HashMap to store numbers and their indices.

class Solution {
    public int[] twoSum(int[] nums, int target) {
        HashMap<Integer, Integer> map = new HashMap<>();
        for(int i = 0; i < nums.length; i++){
            int diff = target - nums[i];
            if(map.containsKey(diff)){
                return new int[]{map.get(diff), i};
            }
            map.put(nums[i], i);
        }
        return new int[]{};
    }
}


## Dry Run
nums = [2,7,11,15], target = 9  
2 → store  
7 → found 2 → answer

## Time Complexity
O(n)

just trace out in notes..
given nums=[2,7,11,15]

hashmap is something that store unique values.

when i=0

diff=9-2

check if our map contains diff.

if it contains just return the index of diff in hashmap and current index.

if not add the current indexed element into our map.

so here our map is empty there is no element ..we just put the current element in our map.

so far we have element 2 in our map.

when i=1

element=7

diff=9-7

diff=2

our map contains element 2.

yes we got the value

just return [0,1]

## concepts

hashmap

map related functions

1.map.put(nums[i],i);--> this line stores a value and its index into hashmap.

2.map.containsKey(diff)-->this lines checks whether we have diff element in our map or not.

3.return new int[]{map.get(diff), i};--> here,new int[] creates an array of integers and puts values inside.

here we are actually creating new array because in java arrays are objects.inorder to return it 

we must create it first .

that is the reason why we use new int[] and then we use curly braces{map.get(diff),i}

The {} are used to put values inside the array at the time of creation.
