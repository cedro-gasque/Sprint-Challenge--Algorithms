#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a) O(n^3) due to the only loop being the while loop, the only factor involving n is n * n * n, or n^3.


b) I thought this was going to be O(n^2) at a glance, but I think it may be something closer to O(n log n)?

The logic here is that it would be O(n^2) if j were just incremented, i.e. the center loop were just a for loop, but j is actually multiplied by 2, which makes me think there's a logarithm involved as due to how much faster powers of 2 scale, it'll scale slower than linear time complexity.


c) O(n), it just decrements the number every time so it's only running the function `bunnies` times.

## Exercise II
I would use a binary search algorithm. The first egg I drop will be at n/2, then if it breaks, I know the egg break is below the middle story, and if it doesn't break, I know the egg break is above the middle story.

Now, I know that the middle floor _could_ be the floor I'm looking for, but I plan on that being a default case that I'll get to later.

Once I decide which half to check, I'd recurse the algorithm on that floor range, with a base case of 0 and 1 floor ranges to some null value I can easily detect or return their own floor, respectively.

That value passes up the grapevine, and at the original recursion (and every lower recursion), if the middle floor is either lower than the value returned by the recursion or the recursion returns nothing (i.e. the middle floor is the lowest floor the egg breaks on, so the lower floors would return nothing), that is the value returned, otherwise the other value is returned.

This algorithm is O(log n) as it's a binary search algorithm.
