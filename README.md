# TJ-Tasks-2024--Naveenkumar- task_1
## Thought Process:
To generate Pascal's Triangle in Java using ArrayList, we need to understand its structure first. Pascal's Triangle is a triangular array where each number is the sum of the two numbers directly above it. The first and last elements of each row are always 1.

The idea is:
The first row is [1].
Each subsequent row is built by taking the previous row, adding a 1 at the start and end, and filling in the middle by adding pairs of adjacent numbers from the previous row.

## Approach:
# Initialization:
We start with the first row as [1].
We create an outer list (a list of lists) to store all the rows. 
Building each row:

For each subsequent row, we begin with [1].
For rows after the first, use the previous row to calculate the values of the current row. Each value is the sum of two adjacent elements from the previous row.
End the row with a 1.
Add the row to the outer list.

## Edge case:
If n (number of rows) is 0, the output is an empty list.

**Time and Space Complexity:**

**Time Complexity:**
For each row, we iterate over the previous row to compute the current row.
The number of elements in row i is i + 1, and the total number of elements in the triangle is the sum of the first n natural numbers, which is O(n^2).
Thus, the time complexity is O(n^2), where n is the number of rows.

## Space Complexity:
We are using an ArrayList to store the triangle, and the space needed for the output is also proportional to the number of elements in the triangle.
The space complexity is O(n^2) because we store all rows in the triangle.

## Challenges Faced:
**Understanding Indexing**:
One challenge was correctly indexing into the previous row to compute the values of the current row. Ensuring that the indices align correctly to sum the two adjacent numbers took some thought.

Edge Case:
Handling the case where numRows is 0 or 1 required careful consideration to avoid index errors or incorrect results.
Efficient Summation:

Another challenge was optimizing the sum calculation between two adjacent elements, but this was managed by directly accessing the previous row using get() method.


![image](https://github.com/user-attachments/assets/37b9f2bd-04aa-4229-8a33-2b3e360ace89)
