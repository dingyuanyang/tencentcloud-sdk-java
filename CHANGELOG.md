### 3.1.0 (2020-02-18)

之前我们将各产品接口定义的数值型参数，都统一实现为Integer。但是实际使用中，我们发现很多整形数值溢出的情况，业务实际是使用了64位整数。最开始我们对发现的例子做了特殊处理，改为了Long型。后来发现越来越多，特殊处理已经不太现实，于是我们挑选了部分使用较为活跃的产品，全部修改为Long型，经过半年左右并无收到负面反馈。因此这次冒险全部修改为Long型。

如果您从3.0.x版本升级到了3.1.x版本，将会面临兼容型问题。您需要重新编译项目，将使用到的接口定义中的Integer转变为Long进行处理。
