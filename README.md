# React getting started
了解学习React。

####What is React
[React](https://facebook.github.io/react/)

一个用于构建用户界面的JavaScript库。  
React是一个框架吗？

* 快速渲染
* 组件驱动

操作DOM很慢  
![html-div](https://raw.githubusercontent.com/KaiZhang890/react-getting-started/master/html-div.png)

>所谓的 Virtual DOM 算法。包括几个步骤：  
>1. 用 JavaScript 对象结构表示 DOM 树的结构；然后用这个树构建一个真正的 DOM 树，插到文档中。  
>2. 当状态变更的时候，重新构造一棵新的对象树。然后用新的树和旧的树进行比较，记录两棵树差异。  
>3. 把2所记录的差异应用到步骤1所构建的真正的DOM树上。  
>[怎么更好的理解Virtual DOM](https://www.zhihu.com/question/29504639)

在一个React应用中，你应该把自己的网站、页面伸直一个功能分解为一个个更小的组件。

>We have components and fast rendering - but why is it a game changer?  
>Because React is mainly a concept and a library secondly.  
>[the react way getting started tutorial/](https://blog.risingstack.com/the-react-way-getting-started-tutorial/)

####How to use

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Simple</title>
  </head>
  <body>
    <div id="container"></div>

    <script src="./js/react.min.js"></script>
    <script src="./js/react-dom.min.js"></script>
    <script>
      var HelloMessage = React.createClass({
        render: function render() {
          return React.createElement("h2", null, "Hello World!");
        }
      });
      
      ReactDOM.render(
        React.createElement(HelloMessage, null),
        document.getElementById('container')
      );
    </script>
  </body>
</html>
```
    
### License
[WTFPL (Do What The Fuck You Want To Public License)](http://www.wtfpl.net)