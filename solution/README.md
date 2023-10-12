# The Star
The Star is the card of hope. In the darkest of nights there is a light that shines the path to home.The Star is inspiration, motivation and gives us strength to move forward.
- Cypherpunk 2077 (Tarot cards)

`Level:` Hard

## Solution
First, I want you to read: https://pillow.readthedocs.io/en/stable/releasenotes/9.0.0.html#restrict-builtins-available-to-imagemath-eval

You have only one hint: 1718378855 can be converted to hex, and then you can convert it to text. You will find that the result is flag (integer > hex > text), which means your flag is in the expression variable. By this information, you may run main.exe and enter the following inputs:
- 1
- 1
- print(
- )

Then you will have your flag on the screen, but why?

In PIL library before version 9.0.0, it allowed you to perform Python code inside the ImageMath.eval(). So, you may print that value instead of the expression without using a real math expression. Read more about it here: https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2022-22817


The flag is: `The Magician`

