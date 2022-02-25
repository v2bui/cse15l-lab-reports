# <center> Week 8 Lab Report 4 </center>
## <center> Vuong Bui </center>
[My Markdown-Parse Repository](https://github.com/v2bui/markdown-parse)
[Reviewed Markdown-Parse Repository](https://github.com/AnniePhan02/CSE15L-Panther)
## Snippet #1 - My Implementation
* What should be produced: 
* ![Image](SS4-1.png)
* Test Code: ![Image](SS4-4.png)
* My Implementation: ![Image](SS4-7.png)

## Snippet #2 - My Implementation
* What should be produced: 
* ![Image](SS4-2.png)
* Test Code: ![Image](SS4-5.png)
* My Implementation: ![Image](SS4-8.png)

## Snippet #3 - My Implementation
* What should be produced: 
* ![Image](SS4-3.png)
* Test Code: ![Image](SS4-6.png)
* My Implementation: ![Image](SS4-9.png)

## Snippet #1 - Reviewed Implementation
* What should be produced: 
* ![Image](SS4-1.png)
* Test Code: ![Image](SS4-4.png)
* Reviewed Implementation: ![Image](SS4-10.png)

## Snippet #2 - Reviewed Implementation
* What should be produced: 
* ![Image](SS4-2.png)
* Test Code: ![Image](SS4-5.png)
* Reviewed Implementation: ![Image](SS4-11.png)

## Snippet #3 - Reviewed Implementation
* What should be produced: 
* ![Image](SS4-3.png)
* Test Code: ![Image](SS4-6.png)
* Reviewed Implementation: ![Image](SS4-12.png)

## Questions
1. Do you think there is a small (<10 lines) code change that will make your program work for snippet 1 and all related cases that use inline code with backticks?
* No, I don't think there is a small code change that will make the program work. Fixing the program will be more complex because we have to check if a pair backticks are both within a pair of brackets or parentheses or not. Additionally, checking if brackets or parentheses exist within backticks would allow us to not count them as part of link markdown formatting.
2. Do you think there is a small (<10 lines) code change that will make your program work for snippet 2 and all related cases that nest parentheses, brackets, and escaped brackets? 
* Yes, I think there is a small code change that will make the program work. Our code should search if there is another open bracket within the brackets instead of directly looking for "](" in order to locate any nested links.
3. Do you think there is a small (<10 lines) code change that will make your program work for snippet 3 and all related cases that have newlines in brackets and parentheses?
* No, I don't think there is a small code change that will make the program work. Our code currently splits the string into separate lines which doesn't allow our code to find the indices of the "](" and ")" properly if they are on a different line. It will be more complex to have to move to the next line to search for the closing brackets and parentheses.