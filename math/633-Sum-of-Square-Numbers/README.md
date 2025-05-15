🧮 633. Sum of Square Numbers

Problem Statement
Given a non-negative integer c, determine whether there exist two integers a and b such that:
a² + b² = c


🧠 Understanding the Problem
In this problem, we need to find two integers whose squares add up to the given number c.
We’ll use the two-pointer approach, which is commonly applied in array problems, but in this case, we’ll adapt it to work with square numbers.


Strategy
Initialise two pointers:
a = 0 (the smallest possible square root)
b = sqrt(c) (the largest possible integer whose square doesn’t exceed c)

At each step:
Calculate sum = a² + b²
If sum == c, return true
If sum < c, increment a (to increase the sum)
If sum > c, decrement b (to reduce the sum)

Continue the process until a > b.
If no such pair is found, return false.

Example
i) If c = 5
Start with a = 0, b = √5 ≈ 2, so b = 2

Check:

0² + 2² = 0 + 4 = 4 → less than 5 → increment a

1² + 2² = 1 + 4 = 5 → ✅ match found → return true

ii) If c = 4
Start with a = 0, b = √4 = 2

Check:

0² + 2² = 0 + 4 = 4 → ✅ match → return true

💡 If we try b = 3, then 3² = 9 > 4, which already exceeds c.
That's why we initialise b = sqrt(c).


⚠️ Important Notes
We must prevent integer overflow when squaring large numbers.
To handle this, we use long long for variables a, b, and their squares.


✅ Final Thoughts
Since the function returns a boolean, we:

Return true if we find a valid pair (a, b) such that a² + b² = c

If no such pair exists, we exit the loop and return false


<img width="283" alt="image" src="https://github.com/user-attachments/assets/3bb7d3b4-a4f7-41ff-8755-d78e12665f3b" />



  
  

