### json
>   json格式？json对象？json字符串？js对象？一直迷迷糊糊的。  

其实我个人理解  json就是js对象的字符串表示法，来表示js对象的信息。
```javascript
    var obj = {name: 'zhangsan', age: '15'} // js对象
    var json = {'name': 'lisi', 'age': '20'} // json字符串
```
用json来表示js对象，
``` javascript
    json: {'name': 'wangwu'}   <=>  js: { name = 'wangwu' }
```
对象 => JSON 字符串，使用 JSON.stringify() 方法：
``` javascript
    var json = JSON.stringify({a: 'Hello', b: 'World'}); //结果是 '{"a": "Hello", "b": "World"}'
```
JSON => 对象，使用 JSON.parse() 方法：
``` javascript
    var obj = JSON.parse('{"a": "Hello", "b": "World"}'); //结果是 {a: 'Hello', b: 'World'}
```