# js-desktop
简单的桌面弹窗（应用于PHPOK后台程序）

HTML代码里加载：

``` html
<link rel="stylesheet" type="text/css" href="css/window.css" />
<script type="text/javascript" src="js/jquery.js"></script>
<script type="text/javascript" src="js/jquery.desktop.js"></script>
```

初始化运行

``` html
<script type="text/javascript">
$(document).ready(function(){
	$.win2.init({
		'close_tip':'',
		'taskbar':false;
		'taskbar_close':false,
		'win_close':true,
		'win_min':true,
		'win_max':true,
		'win_refresh':true,
		'is_max':true,
		'move':true
	});
});
</script>
```

按钮动作示例：

``` html
<input type="button" value="打开一个窗口" onclick="$.win('测试','about:blank')" />
<input type="button" value="打开百度" onclick="$.win('测试外网','https://www.baidu.com')" />
<input type="button" value="打开本地演示" onclick="$.win('测试演示','test.html')" />
```

解释说明：

> $.win('弹窗的标题','目标地址，支持相对或绝对地址')

初始化变量说明：

> 

 - close_tip：关闭窗口时提示，留空不提示，直接关闭
 - taskbar_close：是否显示任务栏关闭按钮
 - taskbar：是否显示任务栏，当前版本没写好，建议先关闭
 - win_close：关闭按钮是否显示
 - win_min：最小化是否显示
 - win_max：最大化是否显示
 - is_max：默认打开后就是最大化
 - move：是否可移动

 预览截图：
 ![预览弹窗效果截图](https://phpok-manual.phpok.com/20187/18/弹窗.jpg)
