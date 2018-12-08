---
layout:	post
title: 'Sencha ItemId 使用不当一则'
date:	2016-11-02 14:37:00
categories: tech
---

在使用Sencha(ExtJS6)的过程中遇到一个诡异的问题。

往TabPanel中添加一个Panel，添加的时候设置Panel的itemId，为了省事，直接用uuid生成的编号作为itemId的值。
> 诡异的事情发生了。
> 浏览器报错 ：　<label style="color: red;">Ext.Component.constructor(): Invalid component "itemId": "7490b8ce-a0c7-11e6-9eea-b8ca3a7c240a"</label>

这个错误并不是每次必报，偶尔发生。刚开始怀疑是某些资源没有清理，但又找不到具体的问题。把itemId改为id，故障依然。最后跟踪代码，找到抛出异常的这段代码：
```javascript
        //<debug>
        if (!me.validIdRe.test(me.id)) {
            Ext.raise('Invalid component "id": "' + me.id + '"');
        }
        if (!me.validIdRe.test(me.itemId)) {
            Ext.raise('Invalid component "itemId": "' + me.itemId + '"');
        }
        //</debug>
```

跟着查看了一下<label style="color:green;">me.validIdRe</label>的值：
```javascript 
        /^[a-z_][a-z0-9\-_]*$/i
```

明白了，itemId和id只能是字母或下划线开头。为itemId加个字母前缀，问题解决！