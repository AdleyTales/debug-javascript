# JavaScript 调试方法

## 第1种：
```js
  console.log();

  不做赘述，如果这个都不用，洗洗睡吧~.~
```
## 第2种：
```js
  debugger;

  chrome浏览器在执行到该句代码时，立即停止，进入调试模式。然后直接debug，调试代码。
```

## 第3种：
```js
  console.table();

  这个是在某些特定的需求下，使用比较方便。一般也不会使用，纯k-v的数据，如此打印，看起来比较直观。不过是习惯问题，自己喜欢就好。

  // 测试代码：
  let obj = {
    name: '小明',
    age: 22,
    work: 'Front Engineer',
    salary: 21000,
    description: 'I love program',
    hobbies: ['football','reading','computer','mobile'],
    other: {
      a: 1000,
      b: 'bbb',
      c: true
    }
  }

  console.table(obj);

```

## 第4种：
```js

  console.time('useTime');
  console.timeEnd('useTime');
  会计算中间js代码执行的时间。

  //code:
  console.time('useTime');

    let arr = [];
    for (var i = 0; i < 100000; i++) {
      arr.push(i);
    }
    console.log(arr.length);

  console.timeEnd('useTime');
```

## 第5种：
```js

  console.trace('trace');

  追踪代码,可以打印当前的代码被调用的位置和对象

  //code：
  function fn1() {
    console.trace('trace fn')
  }

  function fn2() {
    fn1();
  }

  function fn3() {
    fn2();
    fn1();
  }

  fn3();

```

## 第6种：
```js

  这一种也是我最常用的调试方法：

      借助伟大的Chrome自带的debug功能。

      在Sources里面打开要调试的js代码,打上断点,F10： 单步调试。

      可以与Java代码在Eclipse里面调试一样了，JS调试更加方便快捷。

      推荐指数：★★★★★

```
