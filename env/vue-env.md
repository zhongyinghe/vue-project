1、vue项目中如何热重载?
```
"dev": "webpack-dev-server --inline --hot --progress --config build/webpack.dev.conf.js",
//加上--hot
```

2、如何写公共的js函数?<br>
1)新建common目录<br>
2)新建common.js文件，并写相应的函数
```
//奇数判断
function isOdd(number) {
	return number % 2 === 1
}

//偶数判断
function isEven(number) {
    return number % 2 === 0;
}

export {isOdd, isEven}
```
3)main.js中导入
```
import * as common from './common/common.js'
Vue.prototype.common = common
```
4)组件中使用
```
if (this.common.isOdd(rs.code)) {
}
```
