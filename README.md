# 支付宝小程序转微信33小程序 #

### 说明：

	这是一个将支付宝小程序中的大多数与微信33小程序功能相关，格式相似的api与属性转化为支付包小程序的格式
	其中包含了json、js、wxml的转换，但是转换只是治标并不治本，所以转化结束的源码中的一些错误还是需要靠自己进行解决。
	该程序可以给你的代码迁移省下一部分的精力。

## 环境配置：
	node.js
## 安装 
	npm i ali2wxapp -g

## 使用 

**如果是旧版本请命令行中输入npm update ali2wxapp -g进行更新**

1. 	复制支付宝小程序的源码一份；
2. 	ali2wxapp --getConfig获取配置文件路径 按照需要修改配置并保存
3.  ali2wxapp --start
4. 	等待处理完成。
5. 或者可以通过 ali2wxapp --path path路径   开始转换
	
	
## 注意事项

因为是用正则表达式进行转换，所以已经转换过的文件请不要进行二次转换，防止发生不必要的麻烦。

多发生在js文件中。

## 文件: 
	ali2wxapp.txt //配置
	package.json
	index.js //源码
	lib
	--JSApiPropReplace.js //api属性替换

[点击进入github](https://github.com/kujian/ali2wxapp "ali2wxapp转换")

## 转换原则: 

1. 从wxmp（支付宝小程序）转成antmp（微信33小程序）
2. wxmp有而antmp没有的属性、接口 不进行转换	
3. antmp有而wxmp没有的属性、接口 不进行转换	
4. wxmp中的接口、属性与antmp中的接口、属性 如果**功能相同而名称不同**的则**进行转换**
5. 所有文件大体都有正则表达式进行转换
6. js文件有进行过ast转换 可以转换到方法名称

## 更新: 
	
