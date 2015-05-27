# headImageCliper
javascript头像裁剪上传组件，利用flash在本地进行裁剪后再上传，支持按尺寸预览头像。[查看demo](http://libmw.github.io/2015/05/27/head-image-cliper.html)


## 使用方法

```
window.imageCliper = new HeadImageCliper({
    container: container, //上传界面的容器，原生dom
    flashUrl: '../bin-debug/headImageCliper.swf?v=0527', //上传flash的地址,加上版本号，防止flash被缓存
    width: container.clientWidth, //flash的宽度
    height: container.clientHeight, //flash的高度
    uploadUrl: 'upload.php', //上传路径
    file: 'file', //上传的字段名，默认为file
    isPreview: true, //是否显示预览图
    previewSize: '180|100|50', //预览图尺寸。'200|100'代表显示200*200和100*100的预览图。注意预览图的尺寸如果过大，可能会超出flash的可视范围，此时应该设置不显示预览图或者增大flash的宽高度
    resourceUrl: 'http://127.0.0.1/headImageCliper/demo/' //flash包含的按钮、光标等静态文件的放置路径
});
```

