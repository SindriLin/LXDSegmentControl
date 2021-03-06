# LXDSegmentControl

四种不同样式的分栏控制器。包括点击后移动滑块效果，选中后变色，选中内容放大效果以及按钮分隔效果

# 使用要求
XCode7.0以及以上版本

# 相关类定义

* LXDSegmentControlConfiguration   用来配置分栏控制器的显示属性
* LXDSegmentControl   分栏控制器

# 类型枚举

* LXDSegmentControlTypeSlideBlock   分栏控制器是滑块样式，点击分栏按钮移动滑块
* LXDSegmentControlTypeSelectBlock  分栏控制器是圆角矩形样式，点击分栏按钮切换选中颜色
* LXDSegmentControlTypeScaleTitle   分栏控制器是标题样式，点击分栏按钮放大选中标题
* LXDSegmentControlTypeSeparate	    分栏控制器是分隔样式，每个按钮之间用一个竖线分隔

# 回调方式

* 遵守LXDSegmentControlDelegate协议在实现点击按钮回调方法
* 监听LXDSegmentControlSelectIndexNotification通知，通过LXDSegmentControlIndexKey获取选中下标

# 使用方法

``` objc
		//配置分栏控制器按钮数据数组<br>
		LXDSegmentControlConfiguration * configuration = [LXDSegmentControlConfiguration configurationWithControlType: LXDSegmentControlTypeSlideBlock items: @[@"红", @"绿", @"蓝"]];
		//使用配置对象创建分栏控制器
		LXDSegmentControl * segmentControl = [LXDSegmentControl segmentControlWithFrame: CGRectMake(CGRectGetWidth(self.view.frame) * 0.5f - 100.f, 10.f, 200.f, 30.f) configuration: configuration delegate: self];
```

# 自定义属性

``` objc
		LXDSegmentControlConfiguration * configuration = 				[LXDSegmentControlConfiguration configurationWithItems: items];
		configuration.backgroundColor = [UIColor orangleColor];   		  //分栏控制器背景颜色
		configuration.cornerRadius = 5.f;         //分栏控制器圆角半径
		configuration.cornerWidth = 0.5f;         //分栏控制器边缘宽度
		configuration.itemBackgroundColor = [UIColor blueColor];  		  //分栏按钮背景颜色
		······
		LXDSegmentControl * segmentControl = [LXDSegmentControl segmentControlWithFrame: CGRectMake(CGRectGetWidth(self.view.frame) * 0.5f - 100.f, 10.f, 200.f, 30.f) configuration: configuration delegate: self]
```

[我的博客][http://www.jianshu.com/users/0cf7d455eb9e/latest_articles]
