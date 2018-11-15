# mobxCodeLearn
学习mobx源码过程
# 找到入口
* 打开node_modules 找到mobx包，在package.json 搜索main ，找到lib/mobx.js 
* mobx 将所有的api通过exports.*** 导出
* 从observable 开始看起(observable api 的作用就是将数据变为可观测的数据)，可以发现 var observable = createObservable;
* 然后可以找到方法 function createObservable(){}， 
* createObservable(v,arg2,arg3) 有三个参数，先只关注v这个参数 从createObservable 函数中可以看到，首先判断v是否是一个已经可观测的数据（通过 isObservable 方法），如果是直接返回v，如果不是，继续执行下面的方法， 通过 isPlainObject 函数 判断 v 是否是空的 或者是否是一个 object ，
* 
