It is very easy to check if an individual scene is a palindrome, then say "YES". The rest of the editorial will assume no single scene is a palindrome.

Assume there exists some palindromic subsequence. Now, consider what would happen if we only chose the leftmost and rightmost scenes as a new subsequence. Let's enumerate what the leftmost and rightmost scenes could be:
- $xy$ and $yx$: forms $xyyx$, a palindrome
- $xyz$ and $yx$: forms $xyzyx$, a palindrome
- $xyz$ and $zyx$: forms $xyzzyx$, a palindrome
- $xy$ and $zyx$: forms $xyzyx$, a palindrome

We can see that if some palindromic subsequence exists, you can construct another palindromic subsequence by just choosing the two endpoint scenes. This implies if a palindromic subsequence exists, there must exist a palindromic subsequence formed by two scenes.

You can check for palindromic subsequence formed by two scenes using a hashing method and some casework. The time complexity is thus $\mathcal{O}(n)$.