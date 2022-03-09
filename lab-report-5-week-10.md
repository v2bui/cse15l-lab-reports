# <center> Week 10 Lab Report 5 </center>
## <center> Vuong Bui </center>
## How I Found the Tests with Different Results
1. I ran `bash script.sh > sol.txt` in Joe's markdown-parse repository and copied sol.txt to the main directory.
2. I ran `bash script.sh > my.txt` in my markdown-parse repository and copied my.txt to the main directory.
3. In the main directory, I ran `diff sol.txt my.txt` to find the tests with different results.
## Test #1
* Test: ![Image](SS5-1.png)
* Result: ![Image](SS5-2.png)
* My implementation, `[]`, is correct because `/uri` should not be considered a link since there is a space between the closing bracket and open parentheses.
* ![Image](SS5-3.png)
* In this part of the getLinks method in Joe's markdown-parse, the bug in the code is that there is no check to see if openParen is one index greater than nextCloseBracket.
## Test #2
* Test: ![Image](SS5-5.png)
* Result: ![Image](SS5-4.png)
* Both implementations are incorrect because the link that should be returned is `/uri`. This is because this test is hyperlinking `/uri` to an image of `moon.jpg`.
* ![Image](SS5-6.png)
* ![Image](SS5-7.png)
* In the isOfLinkForm method in my markdown-parse (first image), the bug is that after finding the first open bracket, the code immediately looks for `](` without checking if there are any other open brackets before it. This causes the code to miss the nested image within the brackets. When looking at this while loop of Joe's getLinks method in his markdown-parse (second image), there is no check to see if there is a `!` before the brackets, which would make it an image rather than a link. Because of this, his code mistakes the image file as the link to be returned.
