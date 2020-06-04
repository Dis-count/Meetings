在各个象限生成一个约束，这样可以确保一个可行域，但是不是对于n维空间需要2^n个约束需要考虑。

删除了x大于零的约束。

如何给定一个可行域内的解比较重要。

对于给定 x0 = x* 结果必然是零，这一点正确。

则对于在 x* 处的微小扰动，可能存在直接一刀切的改变量会小于这样修改，但一刀切会不稳定。

比较了 只增大A 和 使用绝对值的方法 绝大多数情况下 两者相等，为什么不相等还在想。


有这么几种思路去构造一个可行域：
添加约束：
如果已经有了一个封闭可行域，则求解得到最优解，在最优解处向可行域内取出一个可行解，再计算得到一个过该可行解的一个约束。
减少约束：
首先生成大量的约束，需要保证既有可行解也不是最优解不存在的情况，不是那么好生成的。如果已经有了的话，可以利用不可行原因，删选掉不可行约束。但这种方法局限性较多。

如何形成一个封闭的可行域需要考虑。

对于各个lambda的跳转如何去做。

将A单位化，计算对偶变量，找出 lambda最小的约束，剔出出去，下一循环中对应最优解的lambda 对应约束加入
当所有都循环过后，返回最小值。

找到某种条件，使得这种方法优于 一刀切的方法


所以现在你明白了为什么那篇文章给出一个看似很奇怪的一个可行域了。以及为什么不给定象限处大于零了。