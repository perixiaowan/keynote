# 十九大报告解读
<p>编程语言：R</p>


----

## [十九大报告全文](http://www.liuxiaowan.com/shijiudaCloud/shijiuda-quan.txt)

----

## 入口

![党徽](http://www.liuxiaowan.com/shijiudaCloud/)

----

## 部分代码

```十九大
/*
  将十九大内容下载，存储，读取文件，对内容进行分词，并计算词频使用wordcloud2包将其显示在党徽图标中
*/
text=read.table(file.choose())
text=as.list(text)[[1]]
text=as.character(text)
aa=unlist(segment(text,worker()))
b=as.data.frame(table(aa))
prep=c('的','和','是','在','要','为','我们','以','把','了','到','上','有','不','对','大','从','各','而')
f=b[-which(apply(b['aa'],1,function(x)any(x==prep))),]
ff=f[-which(apply(f[2],1,function(x)any(x<=1))),]
wordcloud2(ff,figPath='danghui.jpg',size=2,color='yellow',backgroundColor='red')
```
----

## 其他生成效果图

### [五角星](http://www.liuxiaowan.com/shijiudaCloud/wujiaoxing.html) & [党字](http://www.liuxiaowan.com/shijiudaCloud/dangzi.html)

----

## Thanks

### [返回首页](http://www.liuxiaowan.com/keynote/)