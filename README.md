# mobxCodeLearn
学习mobx源码过程
# 找到入口
* 打开node_modules 找到mobx包，在package.json 搜索main ，找到lib/mobx.js 
* mobx 将所有的api通过exports.*** 导出
* 从observable 开始看起，可以发现 var observable = createObservable;
* 然后可以找到方法 function createObservable
