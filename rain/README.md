# Rainwater Retention Calculation

## Project Overview

This project aims to calculate the amount of rainwater that can be retained between walls of varying heights, as represented by a list of non-negative integers. Each integer in the list corresponds to the height of a wall with a unit width of 1. This calculation simulates how water would accumulate between these walls after it rains, assuming that the ends of the list are not walls and thus cannot retain water.

## Function Prototype

def rain(walls)


### Parameters

- `walls`: A list of non-negative integers. Each integer represents the height of a wall.

### Returns

- An integer indicating the total amount of rainwater retained between the walls.

### Assumptions

- The list can contain zero or more integers.
- If the list is empty, the function should return 0.
- The ends of the list (before index 0 and after index `walls[-1]`) are not considered walls and will not retain water.



## Implementation Details

The `rain` function calculates the water retained by following these steps:

1. **Initialize two pointers**: `left` and `right`, starting at the beginning and end of the list, respectively.
2. **Track the maximum heights** seen from the left (`left_max`) and right (`right_max`).
3. **Iterate through the list** while `left` is less than `right`:
   - Update the `left_max` or `right_max` based on the current height.
   - Calculate water retained at each position based on the minimum of `left_max` and `right_max`.
   - Move the pointer (`left` or `right`) towards the center based on the heights to ensure all positions are processed.
   This method ensures efficient calculation with a time complexity of O(n), where n is the length of the list.

  
  ## Author
  Yvette Kwizera

  

