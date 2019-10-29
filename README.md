# scripts_demo

## 变量

### 变量的声明方式
- let ( 出于这些以及其他原因，我们建议您在代码中尽可能多地使用 let，而不是 var。)
- var
- 参考：https://developer.mozilla.org/zh-CN/docs/Learn/Getting_started_with_the_web/JavaScript_basics
- [var_与_let_的区别](https://developer.mozilla.org/zh-CN/docs/Learn/JavaScript/First_steps/Variables#var_%E4%B8%8E_let_%E7%9A%84%E5%8C%BA%E5%88%AB)
- 常量用于存储不希望更改的数据，用关键字 const 创建，本例中用常量来保存对界面元素的引用。

### 变量注意事项
- JavaScript 对大小写敏感，myVariable 和 myvariable 是不同的。

## 注释
- 单行注释：// aaa
- 多行注释：/* aaa */

### 类型
- String
- Number
- Boolean：true/false
- Array
- Object

## 运算符
- 加：+（对数字进行加法运算，对字符串进行连接）
- 减：-
- 乘：*
- 除：/
- 赋值：=
- 严格等于：===
- 不等于：!==
- 取非：!+
- 大于：>
- 小于：<
- 复合操作符：+=，-=，*=，/=
- 自增操作符：++
- 自减操作符：--
- 幂运算：**
- 求余(有时候也叫取模)：%

```js
guessCount++;
```

### 运算符注意事项：
- 优先级
- 您可能会看到有些人在他们的代码中使用==和!=来判断相等和不相等，这些都是JavaScript中的有效运算符，但它们与===/!==不同，前者测试值是否相同， 但是数据类型可能不同，而后者的严格版本测试值和数据类型是否相同。 严格的版本往往导致更少的错误，所以我们建议您使用这些严格的版本。

## 条件语句
- if ... else ...
```js
let iceCream = 'chocolate';
if (iceCream === 'chocolate') {
  alert('我最喜欢巧克力冰激淋了。');    
} else {
  alert('但是巧克力才是我的最爱呀……');    
}
```

```js
if (userGuess === randomNumber) {
    lastResult.textContent = '恭喜你！猜对了';
    lastResult.style.backgroundColor = 'green';
    lowOrHi.textContent = '';
    setGameOver();
  } else if (guessCount === 10) {
    lastResult.textContent = '!!!GAME OVER!!!';
    setGameOver();
  } else {
    lastResult.textContent = '你猜错了！';
    lastResult.style.backgroundColor = 'red';
    if(userGuess < randomNumber) {
      lowOrHi.textContent = '你猜低了！';
    } else if(userGuess > randomNumber) {
      lowOrHi.textContent = '你猜高了';
    }
  }
  ```

## 函数（function）
- 内置函数：alert，document.querySelector...
- 自定义函数：return 语句告诉浏览器当前函数返回 result 变量。

```js
function multiply(num1, num2) {
  let result = num1 * num2;
  return result;
}
```

## 事件
```js
document.querySelector('html').onclick = function() {
    alert('别戳我，我怕疼。');
}
```

```js
guessSubmit.addEventListener('click', checkGuess);
```

## 类型转换：String转换成Number
```js
let userGuess = Number(guessField.value);
```

## 循环（Loop）
```js
for (let i = 1; i < 21; i++) { 
    console.log(i); 
}

let resetParas = document.querySelectorAll('.resultParas p');
for (let i = 0 ; i < resetParas.length ; i++) {
  resetParas[i].textContent = '';
}
```

## 数字
- 如果可以的话， Number 对象将把传递给它的任何东西转换成一个数字。
```js
let myString = '123';
let myNum = Number(myString);
typeof myNum;
```

- 另一方面，每个数字都有一个名为 toString() 的方法，它将把它转换成等价的字符串。
```js
let myNum = 123;
let myString = myNum.toString();
typeof myString;
```

- 拥有方法：
    - toString()

## 字符串 String
- 拥有属性：
    - length
- 拥有索引：browswerType[0]
- 拥有方法：
    - indexOf('value')：返回字符串的起始位置
    - slice(0,3)：提取字符串，提取从第一个位置开始，直到但不包括最后一个位置。
    - slice(2):提取字符串，从第二个位置到最后
    - toLowerCase()：转换为小写字符
    - toUpperCase()：转换为大写字符
    - replace('moz','van'):替换字符串，返回一个新的字符串
    - split(',')：按照分隔符进行拆分，变成数组

## 数组
- 属性
    - length
- 方法：
    - join(',')：数组按照分隔符组织成字符串
    - toString():变成字符串，默认用分隔符：,
    - push()：在数组末尾添加一个项目，返回插入项目的位置
    - pop()：在数组末尾删除一个项目，返回删除的项目
    - unshift()：在数据开头添加一个项目，返回插入项目的位置
    - shit()：在数据开头删除一个项目，返回删除的项目
