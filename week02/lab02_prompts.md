# Lab 02 CLI comparison journal

Do not include passwords, tokens, API keys, or complete authentication output.

## Tool check

### GitHub Copilot CLI

I installed and authenticated GitHub Copilot CLI successfully. I verified the installation using the version command, and the installed version is 1.0.83.

### Antigravity CLI

I installed and authenticated Antigravity CLI successfully. I verified the installation using the version command, and the installed version is 1.1.27.

## Shared task

Write a Python function named count_vowels(text: str) -> int that counts the vowels a, e, i, o, and u in the given text without regard to case. Do not count y as a vowel. Return the total number of vowels. Explain your approach briefly.

### Shared prompt

Paste the exact prompt you submitted to both CLI tools.

```text
Write a Python function named count_vowels(text: str) -> int that counts the vowels a, e, i, o, and u in the given text without regard to case. Do not count y as a vowel. Return the total number of vowels. Explain your approach briefly.
```

### Copilot CLI observations

Copilot CLI suggested converting the text to lowercase and then using a generator expression with sum() to count characters that appear in the string "aeiou". I thought the approach was simple and easy to understand. I would still want to verify that it works correctly with uppercase letters, empty strings, and text containing y. I also noticed that the solution was concise and directly followed the requested function signature.

### Antigravity CLI observations

Antigravity CLI suggested converting the text to lowercase and creating a set containing "a", "e", "i", "o", and "u". It then used a generator expression with sum() to count the vowels. The explanation was clear and helped me understand why uppercase vowels would still be counted. I would verify its behavior with an empty string, uppercase letters, and words containing y to make sure it completely follows the requirements.

### Comparison

Both Copilot CLI and Antigravity CLI produced correct and understandable approaches for the count_vowels function. Both converted the text to lowercase and used sum() with a generator expression, so they handled uppercase and lowercase vowels without needing separate checks. The main difference was how they stored the vowels. Copilot CLI checked whether each character was in the string "aeiou", while Antigravity CLI created a set containing the five vowels and checked membership in that set. Copilot's solution was slightly shorter and very easy to read, while Antigravity's solution made the collection of vowels more explicit. Neither approach counted y, which matched the requirement. I would choose Copilot's approach for this small function because it is concise and clear, although both solutions should produce the same result. I would still verify the final implementation using the provided tests before deciding that it is correct.

## Test-guided implementation
I ran the provided pytest tests after implementing all three functions in lab02.py. The tests for make_greeting, is_even, and count_vowels all passed. The tests checked simple, multiword, and empty names for the greeting function, positive, zero, and negative numbers for the even-number function, and case-insensitive vowels, text without vowels, and empty text for the vowel function. This confirmed that the implementations matched the required function contracts. I did not need to revise the Python functions because all nine function tests passed on the first test run. The four failures I received were related to unfinished template markers and required reflection sections in lab02_prompts.md, rather than the Python implementation. Based on the test results, I kept the function implementations unchanged and focused on completing the journal correctly.

## Preferred tool combination

I found that each tool was useful in a different way. Browser chat was the easiest for asking questions, troubleshooting problems, and getting step-by-step explanations when I was unsure what to do. GitHub Copilot in VS Code is useful when I am already working directly inside a code file because it can suggest code without leaving the editor. Copilot CLI was helpful because it worked from the repository and gave a concise solution, although its session interface was a little harder for me to navigate. Antigravity CLI also gave a correct solution and a clear explanation, but its setup and terminal interface took more time to get comfortable with. Right now, I prefer using browser chat together with Copilot in VS Code because that combination feels the easiest and most practical for me. I could change my choice if I become more comfortable using CLI tools or if I work on a larger project where repository-level assistance becomes more important.
