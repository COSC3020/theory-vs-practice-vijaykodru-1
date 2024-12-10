# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

  i. it is misleading because it ignores the constants which can be a major because they can cause significant impact on the performance of the code which misleads us in calculating the speed of the algorithm

  ii. Asymptotic analysis focuses on how algorithms perform as input size grows large, but for small input sizes and implementation details have a bigger impact on performance. So, for small $n$, the asymptotic behavior (described by $n_0$) is often ignored because it doesn't accurately reflect the actual performance.

  iii. Asymptotic analysis often focuses only on the worst-case scenario (upper bound). For example, a runtime of $n^2 + n^3$ may be simplified to $O(n^3)$, ignoring the impact of the $n^2$ term, which can significantly differ in practice.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

  Given that the time it takes to find a particular element in a binary search tree of size 1000 is 5 seconds. From this we can derive the time it takes to find somthing in a tree with size of 10000. It is done as follow:

  $T(n)$ is the time it takes 

  $T(n)/T(n_0) = log(n)/log(n_0)$

  $T(10000)/T(1000) = log(10000)/log(1000)$
  
  $T(10000)/5 = 4/3$ because we know that log(10000) = 4 and log(1000) = 3
  
  $T(10000) = 20/3$

  $T(10000) = 6.67 seconds$


- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

  i. The performance can be influenced by the hardware specifications, such as CPU speed, memory, or cache size, which are not accounted for in asymptotic analysis. Because the code might be running on a completely different machine for each case where the time might differ based on how the machines can handle the program. 

  ii. If the elements are large, like long strings or complex objects, comparing them might take longer, increasing the search time beyond what asymptotic analysis predicts. For exmaple, if we have a input list of 1000 integers when compared input list of 10000 strings this would take longer than the calculated time because comparing the strings take linear time vs comparing the integers is constant.

  iii. If the machine that the code is being run on has other programs running simultaneously this would make the difference in the time complexity.

Add your answers to this markdown file.


I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice
