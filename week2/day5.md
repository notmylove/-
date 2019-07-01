# 第五天6.28
记录一下一位学员提到的有意思的问题

**需求：** 考察个人的业绩变化对总体变化的贡献能力

这里业绩的指标是签单率 = 签单量/订单量，由于不能单纯的只考虑签单率的变化，因此可以考虑构造一个关于签单量与订单量的新指标。有一个有意思的推导过程：

## 符号说明

上月 ：

业务人员1 ：签单量 a0 订单量 b0

业务人员2 : 签单量 a1 订单量 b1

.....

下月：

业务人员1 ：签单量 a0' 订单量 b0'

业务人员2 : 签单量 a1' 订单量 b1'

.....

A1 = a0 + a1 + ... ,
B1 = b0 + b1 + ... ,
A2 = a0' + b1' + ... ,
B2 = b0' + b1' + ... ,

## 推导过程
因此， 总的签单率的变化 A2/B2 -A1/B1 = ...... = (B1(a0' - a0) - A1(b0' -b0))/B1B2 + ......

## 分析
也就是说总的签单率的变化可以化成每个人的影响之和，其中业务人员1的影响为：

(B1(a0' - a0) - A1(b0' -b0))/B1B2

业务人员2的影响为：

(B1(a1' - a1) - A1(b1' -b1))/B1B2

......

因此考虑式子：**(B1(a0' - a0) - A1(b0' -b0))/B1B2** ,进一步简化为 B1(a0' - a0) - A1(b0' -b0)，其中B1>=A1,也就是说考虑一个新指标
B1(a0' - a0) - A1(b0' -b0)，(a0' - a0)为签单量的改变量，(b0' -b0)为订单量的改变量，**B1，A1分别为它们的系数**，且签单量的改变量的比重是要
大于等于订单量的改变量的。因此，通过这个指标来刻画一个业务人员的贡献度。

进一步，指标可以变形为 (a0' - a0) - A1/B1 (b0' -b0)，其中A1/B1 <= 1，考虑将A1/B1固定不变为部门的kpi，如0.95，固定后的好处是可以对比
同一个人在不同期的贡献情况。

## 总结
有一点需要注意的是：签单率越高，难度系数是越大的，也就说30% 到 50%，与70%到90%难度是完全不一样的，而且有一点是
**每个人的签单率非减，总签单率也可能会降低**，因此，我觉得在签单率到底了一个水平后，应该再给个难度系数，这样才会更加合理。
其实我觉得指标没有好坏之分，系数的设计主要还是看业务目标的本质，然后通过自己的专业度去帮助他们通过一个更合理或者说更有价值的指标去观察和分析
目标完成的情况。