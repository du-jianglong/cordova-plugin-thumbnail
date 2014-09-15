# com.sinosoft.cordova.thumbnail

这个插件实现了生成图片缩略图的功能。支持Android 4+和iOS 6+。

使用回调函数的方式：

```
window.Thumbnails.thumbnail(srcPath, width, height, function success(path) {
	console.log("生成的缩略图存放在：" + path);
}, function fail(error) {
	console.error(error);
});
```

promise的方式：

```
window.Thumbnails.thumbnail(srcPath, width, height).then(function(path) {
	console.log("生成的缩略图存放在：" + path);
}, function(error) {
	console.error(error);
});
```

`window.Thumbnails.thumbnail(srcPath, width, height, [options,] successFn, failFn)`的参数讲解：

* `srcPath` 图片路径
	
	支持的路径格式：
	
	* base64方式的图片路径，如：`data:image/gif;base64,111111111`
	* Android路径：cdvfile://localhost/persistent/DCIM/Camera/1395167011485.jpg

* `width` 缩略图的宽度
* `height` 缩略图的高度
* `options` 其他的配置参数对象

	* `toPath` 缩略图存储路径
	* `srcPath` 图片路径
	* `width` 缩略图宽度
	* `height` 缩略图高度
	* `successFn` 生成缩略图成功的回调函数
	* `failFn` 缩略图生成失败的回调函数

* `successFn` 缩略图生成成功的回调函数
* `failFn` 缩略图生成失败的回调函数