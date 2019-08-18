# 如何链接CSS到HTML文件（How to link css to html file）

## HTML文件内链接（inline link & internal link）
- inline link
```css
<h1 style= "color:pink;">This is a pink Heading </h1>
```
- internal link
    1. 在head下方新建一个style标签（The new 'style' tag in the 'head' tag）
    2. 在style标签内用CSS语法写CSS(Write CSS language in 'style')
```css
<html>
    <style>
        body{background-color:pink;}
        h1{
            color:lightblue
        }
        p{
            color:pink
        }
    </style>
    <head>
        <title>Good day </title>

    </head>
    <body>
        <p> method of linking CSS to html by internal link
        </p>
    </body>
</html>

```


## HTML外部链接CSS(External link）
- 这种方法是最好的（the most important and useful method）

在html文件内增加链接（In html file）
```css
<head>
    <link> rel="relationName" href="cssFileName"
    </link>
</head>
```
## 补充说明 （链接html后，如何实现相应的效果）

## 使用`element`作为selector
```css
h1{
    color: purple; font-family: "Trebuchet MS",verdana,sans-serif ;
}
```
以上的例子通过```h1```这个selector,把CSS的效果与html文件中的`h1`相对应

## 使用`id`或`class`作为selector
```css
/* 我是id，我前面用#表示 */
#myHeader {
  background-color: lightblue;
  color: black;
  padding: 40px;
  text-align: center;
}

/* 我是class，我前面用.表示 */
.city {
  background-color: tomato;
  color: white;
  padding: 10px;
} 
```

```html

<!-- 我是id，一个我只能对应一个element -->
<h1 id="myHeader">My Cities</h1>

<!-- 我是class，一个我可以对应多个element -->
<h2 class="city">London</h2>
<p>London is the capital of England.</p>

<h2 class="city">Paris</h2>
<p>Paris is the capital of France.</p>

<h2 class="city">Tokyo</h2>
<p>Tokyo is the capital of Japan.</p>
```

## `id`功能延伸：如何用`id`实现页面的跳转 （Markdown可用）

1. 创建一个bookmark

```html
<h2 id="#link">第二章<!--我是目录--></h2>
```

2. (在同一个页面内）跳转

```html
<a href="#link">第二章<!--我是正文--></a>



