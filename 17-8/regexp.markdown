# 常用的正则 
一直就在用可一直记忆不清楚的知识点。于是，花点时间简单的整理一下。
### 创建表达式  
* 内建构造器RegExp()创造   
    var re = new RegExp("some regular expression", 'gmi');  
* 正则文本标记法   
    var re = /some regular expression/ig;
### RegExp属性  
>
    -g global [全局匹配]  [默认false]
    -i ignoreCase [忽略大小写 ]  [默认false]
    -m multiline [跨行搜索]  [默认false]
    -u Unicode [处理编码 es6]
    lastIndex  [搜索开始的索引位]  [默认0]
    spurce [存储正则的匹配模式]
### 相关方法 
>   
    test():    reg.test("str")            true / false
    exec():    reg.test("str")            返回一个匹配到的字符串组成的数组 / null
    search():  str.search(reg)            返回结果数组中只有一个匹配对象 / null
    match()：  str.search(reg)            返回匹配字符串的索引位置number / -1
    replace()：str.replace(reg,"reStr")   返回匹配的字符串
    split():   str.splite(reg)            切割成新数组

** replace **  
```javascript
    // /d 匹配数字
    var str = "abcdw21312";
    str.replace(/\d/g,"!"); // abcdw!!!!!
    // $&代替所找到的文本
    str.replace(/(\d)/g,"*$&") // abcdw*2*1*3*1*2
    // $n代表找到的分组(分组即正则中带1括号的为1个分组)
    var email = "qqqian0819@gmail.com";
    email.replace(/(.*)@(.*)\..*/,"$1"); // qqqian0819
```
#####  剩下的es6 的东西以后再补充，毕竟现在用的正则就已经很强大了