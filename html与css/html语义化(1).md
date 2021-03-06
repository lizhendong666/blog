# 场景
关于html语义化问题，听到过各种各样的解释方式。最近听到一个大神的解释，觉得表好，记录一下。


##1、作为自然语言延伸的语义类标签

### 1.1 ruby
在日文，有一个语法现象叫ruby（大名鼎鼎的 ruby 语言就是依次命名的。）    
这是一种给特定文字加注解的方式。html5对这种现象进行了支持。
> 例如开玩笑聊天，中经常用到的。 “真开（shang）心！”，就属于ruby这种语法现象。

```
<ruby>
  <rb>漢</rb>
  <rp>(</rp>
     <rt>han</rt>  
  <rp>)</rp>
</ruby>
```
<ruby>
  <rb>漢</rb>
  <rp>(</rp>
     <rt>han</rt>  
  <rp>)</rp>
</ruby>


### 1.2 em
比如这样一句话，"我今天吃了一个苹果"。    
在不同上下文中，可能会有不同的表达重点。    

> “你最近吃苹果了么？”    
> “我今天吃了一个苹果！”。     

此时重音是，“今天”。

> “昨天吃了一个香蕉,我今天吃了一个苹果”。

此时重音是，”苹果“

> “你吃了几个苹果？”“我今天吃了一个苹果”   

此时重音是，“一个”

---
此时，需要em标签，标出重音（表达的重点），来消除歧义。    
```
我<em>今天</em>吃了一个苹果。
我今天吃了一个<em>苹果</em>。
我今天吃了<em>一个</em>苹果。
```

##2、作为标题摘要的语义类标签
> 语义化的 HTML 能够支持自动生成目录结构，HTML 标准中还专门规定了生成目录结构的算法，即使我们并不打算深入实践语义，也应该尽量在大的层面上保证这些元素的语义化使用。
### 2.1、标题与结构
```
<h1>第一季</h1>
<p>....</p>
<h2>第一集</h2>
<p>...</p>......
```
### 2.2、副标题
```
<hgroup>
  <h1>Welcome to my WWF</h1>
  <h2>For a living planet</h2>
</hgroup>
```
### 2.3、section
section 会使其内部的 h1~h6 下降一级。    
这样就可以完全使用h1标签了。通过section之间的嵌套，完成不同级别的效果。     
这样做的好处是，可以让【文章结构】跟【html结构】尽最大可能的保持一致。
```
<h1>第一季</h1>
<section> 
   <h1>第一级</h1>
</section>
```



## 3、作为结构的语义类标签
```
<body>
    <header>
        <nav>
            ……
        </nav>
    </header>
    <aside>
        <nav>
            ……
        </nav>
    </aside>
    
    <section>……</section>
    <section>……</section>
    <section>……</section>
    
    <footer>
        <address>……</address>
    </footer>
</body>
```