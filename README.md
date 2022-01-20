# flutter 安卓桌面小部件

## 使用插件 
home_widget: ^0.1.2+1
workmanager: ^0.2.2

## 步骤
1. 创建 android/app/res/layout/example_layout.xml 文件
    - 创建小部件布局
2. 创建 android/app/res/xml/ home_widget_example.xml 文件
    ```
	<?xml version="1.0" encoding="utf-8"?>
	<appwidget-provider xmlns:android="http://schemas.android.com/apk/res/android"
    android:minWidth="40dp"
    android:minHeight="40dp"
    android:updatePeriodMillis="86400000"
    android:initialLayout="@layout/example_layout"
    android:resizeMode="horizontal|vertical"
    android:widgetCategory="home_screen">
	</appwidget-provider>
	
3. 添加 WidgetReceiver到AndroidManifest.xml
	```
	<receiver android:name="HomeWidgetExampleProvider" >
    <intent-filter>
        <action android:name="android.appwidget.action.APPWIDGET_UPDATE" />
    </intent-filter>
    <meta-data android:name="android.appwidget.provider"
        android:resource="@xml/home_widget_example" />
		</receiver>
		
4. 创建 kotlin/com/example/fluttertest/HomeWidgetExampleProvider.kt


| 名称 | 测试结果 |
| -- | -- |
| 安卓 | ··|
| 小部件显示排版 | ✅ |
| 小部件点击进入 | ✅ |
| 小部件按钮点击 | ❎ |
| Ios | ·· |
| 未测试 | ❎ |


![图片](http://img1.kllh.vip/981621596388_.pic.jpg)
