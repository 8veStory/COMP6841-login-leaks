# COMP6841-login-leaks
**All three letter segments are part of the password and are guaranteed to be in order
but not necessarily consecutive. There are no repeated characters in the password.**

Solution: build a dictionary of all the letters and their relative position to one another.
As we scan through the words, if a letter is behind another, its position is set to be
behind that letter. All letters which are behind the original letter are also decremented.

This gives us each letter's relative position to one another. If there were enough
word samples, this will be enough to reconstruct the entire password. If not, 
the password will be printed with '/'s inbetween letters the program is
unsure about.
