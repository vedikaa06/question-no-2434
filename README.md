# question-no-2434
Solution to the question no 2434 on leet code 

2434. Using a Robot to Print the Lexicographically Smallest String
You are given a string s and a robot that currently holds an empty string t. Apply one of the following operations until s and t are both empty:

Remove the first character of a string s and give it to the robot. The robot will append this character to the string t.
Remove the last character of a string t and give it to the robot. The robot will write this character on paper.
Return the lexicographically smallest string that can be written on the paper.

Key Concepts:
Count frequency of each character in the string using cnt[].

Use a stack to temporarily hold characters.

Always track the smallest remaining character (minCharacter) that hasn't been fully used yet.

Pop from the stack and add to result if the top of the stack is ≤ smallest remaining character.

🔁 Step-by-Step:
For every character c in the string:

Push it onto the stack.

Decrease its count in cnt.

Update minCharacter to the next smallest character still left in the string.

Keep popping from the stack to result if the top is less than or equal to minCharacter.
