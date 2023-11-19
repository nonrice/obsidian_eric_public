When translated, the notation in this problem asks this: "Find the combined maximal sum of $k$ disjoint subarrays, each of size $m$".

This is a DP problem. Let $dp_{i,j}$ represent the problem on prefix up to $j$ (inclusive) with $k=i$. At any $(i, j)$, you may choose whether or not to construct a subarray with endpoint $j$. Thus the recurrence is:
$$
dp_{i, j} = 
\begin{cases}
0, &\text{if } j<i\cdot m\text{ or }j=0\text{ or }i=0\\\
\mathrm{max}(dp_{i,j-1},dp_{i-1,j}+\displaystyle\sum_{i=j-m+1}^{j}p_i), &\text{otherwise}
\end{cases}
$$
 You can use sliding window method to calculate the summation term. This results in $\mathcal{O}(nk)$ DP.

