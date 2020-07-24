# react原理

## 函数式编程

![image-20200721215926555](C:\Users\30475\AppData\Roaming\Typora\typora-user-images\image-20200721215926555.png)

## vdom和diff算法

![image-20200721220809014](C:\Users\30475\AppData\Roaming\Typora\typora-user-images\image-20200721220809014.png)



![image-20200721220708613](C:\Users\30475\AppData\Roaming\Typora\typora-user-images\image-20200721220708613.png)



![image-20200721221008609](C:\Users\30475\AppData\Roaming\Typora\typora-user-images\image-20200721221008609.png)

## JSX本质

```jsx
// https://www.babeljs.cn/

// // JSX 基本用法
// const imgElem = <div id="div1">
//     <p>some text</p>
//     <img src={imgUrl}/>
// </div>

const imgElem = React.createElement("div", {
    id: "div1"
}, React.createElement("p", null, "some text"), React.createElement("img", {
    src: imgUrl
}));

// // JSX style
// const styleData = { fontSize: '30px',  color: 'blue' }
// const styleElem = <p style={styleData}>设置 style</p>

const styleElem = React.createElement("p", {
    style: styleData
}, "\u8BBE\u7F6E style");

// // JSX 加载组件
// const app = <div>
//     <Input submitTitle={onSubmitTitle}/>
//     <List list={list}/>
// </div>

const app = React.createElement("div", null, React.createElement(Input, {
    submitTitle: onSubmitTitle
}), React.createElement(List, {
    list: list
}));

// // JSX 事件
// const eventList = <p onClick={this.clickHandler}>
//     some text
// </p>

const eventList = React.createElement("p", {
    onClick: this.clickHandler
}, "some text")

// // JSX list
// const listElem = <ul>{this.state.list.map((item, index) => {
//     return <li key={item.id}>index {index}; title {item.title}</li>
// })}</ul>

const listElem = React.createElement("ul", null, this.state.list.map((item, index) => {
    return React.createElement("li", {
        key: item.id
    }, "index ", index, "; title ", item.title);
}));


// // 总结
// React.createElement('div', null, [child1, child2, child3])
// React.createElement('div', {...}, child1, child2, child3)
// React.createElement(List, null, child1, child2, '文本节点')
// // h 函数
// // 返回 vnode
// // patch
```

![image-20200721224509305](C:\Users\30475\AppData\Roaming\Typora\typora-user-images\image-20200721224509305.png)

![image-20200721224739219](C:\Users\30475\AppData\Roaming\Typora\typora-user-images\image-20200721224739219.png)

## 合成事件

![image-20200721225133417](C:\Users\30475\AppData\Roaming\Typora\typora-user-images\image-20200721225133417.png)

![image-20200721225401419](C:\Users\30475\AppData\Roaming\Typora\typora-user-images\image-20200721225401419.png)

![image-20200721230256481](C:\Users\30475\AppData\Roaming\Typora\typora-user-images\image-20200721230256481.png)

## setState和batchUpdate

![image-20200721230526739](C:\Users\30475\AppData\Roaming\Typora\typora-user-images\image-20200721230526739.png)

![image-20200721230804746](C:\Users\30475\AppData\Roaming\Typora\typora-user-images\image-20200721230804746.png)

![image-20200721231017266](C:\Users\30475\AppData\Roaming\Typora\typora-user-images\image-20200721231017266.png)

![image-20200721231258120](C:\Users\30475\AppData\Roaming\Typora\typora-user-images\image-20200721231258120.png)

![image-20200721231316006](C:\Users\30475\AppData\Roaming\Typora\typora-user-images\image-20200721231316006.png)

![image-20200721231446452](C:\Users\30475\AppData\Roaming\Typora\typora-user-images\image-20200721231446452.png)

![image-20200721231530830](C:\Users\30475\AppData\Roaming\Typora\typora-user-images\image-20200721231530830.png)

![image-20200721231707390](C:\Users\30475\AppData\Roaming\Typora\typora-user-images\image-20200721231707390.png)

![image-20200721231721596](C:\Users\30475\AppData\Roaming\Typora\typora-user-images\image-20200721231721596.png)

![image-20200721231839125](C:\Users\30475\AppData\Roaming\Typora\typora-user-images\image-20200721231839125.png)

## 组件渲染

![image-20200721232012625](C:\Users\30475\AppData\Roaming\Typora\typora-user-images\image-20200721232012625.png)

![image-20200721232439663](C:\Users\30475\AppData\Roaming\Typora\typora-user-images\image-20200721232439663.png)

![image-20200721232604688](C:\Users\30475\AppData\Roaming\Typora\typora-user-images\image-20200721232604688.png)

![image-20200721232730946](C:\Users\30475\AppData\Roaming\Typora\typora-user-images\image-20200721232730946.png)

![image-20200721232836020](C:\Users\30475\AppData\Roaming\Typora\typora-user-images\image-20200721232836020.png)

![](C:\Users\30475\AppData\Roaming\Typora\typora-user-images\image-20200721233157116.png)