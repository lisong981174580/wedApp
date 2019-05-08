### 移动端基本知识

#### 一、 Pixel 移动端开发像素知识

1. px:css pixel逻辑像素，浏览器使用的抽象单位
2. dp,pt:设备无关像素
3. dpr设备像素缩放比 1px = dpr*dpr*dp
4. DPI：打印机每英寸可以喷的墨汁点(印刷行业)
5. PPI：屏幕每英寸的像素数量，既单位英寸内的像素密度


#### 二、Viprwport
> 把页面放在Viprwport里面，完了通过缩放放在视口中（一般为980px)

1. 窗口Viprwport
2. 布局Viprwport
3. meta标签

```
//本人常用的
 <meta name="viewport" content="width=device-width, initial-scale=1, user-scalable=no">

```
```
<meta name="viewport" content="width=device-width, initial-scale=1.0, minimum-scale=0.5, maximum-scale=2.0, user-scalable=yes" />  
在网页的<head>中增加以上这句话，可以让网页的宽度自动适应手机屏幕的宽度。

其中：

width=device-width ：表示宽度是设备屏幕的宽度
initial-scale=1.0：表示初始的缩放比例
minimum-scale=0.5：表示最小的缩放比例
maximum-scale=2.0：表示最大的缩放比例
user-scalable=yes：表示用户是否可以调整缩放比例

如果是想要一打开网页，则自动以原始比例显示，并且不允许用户修改的话，则是：

<meta name="viewport" content="width=device-width, initial-scale=1.0, minimum-scale=1.0, maximum-scale=1.0, user-scalable=no" />  

这样子写后，就可以把一些页头横幅等的图片的宽度都设置成style="width:100%"，整个页面在设备上看起来就是全屏的了。

```

### 三、移动端布局
> 不用固定布局

1. 响应式布局
2. flex弹性布局

### 四、文本溢出

```
    .box{
        //单行文本溢出
        overflow: hidden;
        white-space: nowrap;
        text-overflow: ellipsis;

        //多行文本溢出
        display: -webkit-box !important;
        overflow: hidden;
        text-overflow: ellipsis;
        word-break: break-all;
        -webkit-box-orient: vertical;
        -webkit-line-clamp: 2;
    }
    
```