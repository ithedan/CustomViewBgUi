#####先看两张效果图
#####版本4.4

![4.4.gif](http://upload-images.jianshu.io/upload_images/3523210-b4821a7d8a8dae52.gif?imageMogr2/auto-orient/strip)
#####版本5.0+

![5.0++.gif](http://upload-images.jianshu.io/upload_images/3523210-f563c55512425df1.gif?imageMogr2/auto-orient/strip)

#####看完这两张图后，要实现以上按钮的selector，颜色角度不同的情况下会分别创建不同的selector和shape,,现在只用一个ButtonBgUi就可以达到以上的效果，，再也不用重复的创建selector,老规矩，先看使用方法：

######step1:Add it in your root build.gradle at the end of repositories:
```
allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
```
#####Step 2. Add the dependency
````
dependencies {
	        compile 'com.github.ithedan:CustomViewBgUi:v1.0'
	}
````
######布局中的使用方法
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#f7f7f8"
    android:orientation="vertical"
    tools:context="com.came.customviewbgui.MainActivity">

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginLeft="20dp"
        android:layout_marginRight="20dp"
        android:layout_marginTop="20dp">

        <com.came.viewbguilib.ButtonBgUi
            android:layout_width="0dp"
            android:layout_height="50dp"
            android:layout_marginRight="10dp"
            android:layout_weight="1"
            android:text="充值"
            android:textSize="18sp"
            android:textColor="#ffffff"
            android:clickable="true"
            app:defaultColor="#52adff"
            app:topRightRadius="25dp"
            app:bottomRightRadius="25dp"
            />

        <com.came.viewbguilib.ButtonBgUi
            android:layout_width="0dp"
            android:layout_height="50dp"
            android:layout_marginLeft="10dp"
            android:layout_weight="1"
            android:text="提现"
            android:textSize="18sp"
            android:textColor="#ffffff"
            android:clickable="true"
            app:defaultColor="#52adff"
            app:topLeftRadius="25dp"
            app:bottomLeftRadius="25dp"
            />
    </LinearLayout>

    <com.came.viewbguilib.ButtonBgUi
        android:layout_width="match_parent"
        android:layout_height="50dp"
        android:text="登陆"
        android:textSize="18sp"
        android:textColor="#ffffff"
        android:clickable="true"
        android:layout_marginLeft="20dp"
        android:layout_marginRight="20dp"
        android:layout_marginTop="20dp"
        app:defaultColor="#f7964f"
        app:raoundRadius="5dp"
        />

    <com.came.viewbguilib.ButtonBgUi
        android:layout_width="match_parent"
        android:layout_height="50dp"
        android:text="注册"
        android:textSize="18sp"
        android:textColor="#ffffff"
        android:clickable="true"
        android:layout_marginLeft="20dp"
        android:layout_marginRight="20dp"
        android:layout_marginTop="20dp"
        app:defaultColor="#c95fdc"
        app:pressedColor="#995ae9"
        app:raoundRadius="5dp"
        />

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginLeft="20dp"
        android:layout_marginRight="20dp"
        android:layout_marginTop="20dp">

        <com.came.viewbguilib.ButtonBgUi
            android:layout_width="0dp"
            android:layout_height="50dp"
            android:layout_marginRight="10dp"
            android:layout_weight="1"
            android:text="登陆"
            android:textSize="18sp"
            android:textColor="#ffffff"
            android:clickable="true"
            app:strokeColor="#f7964f"
            app:strokeWidth="0.5dp"
            app:defaultColor="#58cca0"
            app:pressedColor="#2b9d4b"
            app:topRightRadius="10dp"
            app:topLeftRadius="5dp"
            app:bottomLeftRadius="10dp"
            app:bottomRightRadius="5dp"

            />

        <com.came.viewbguilib.ButtonBgUi
            android:layout_width="0dp"
            android:layout_height="50dp"
            android:layout_marginLeft="10dp"
            android:layout_weight="1"
            android:text="注册"
            android:textSize="18sp"
            android:textColor="#ffffff"
            android:clickable="true"
            app:defaultColor="#58cca0"
            app:pressedColor="#2b9d4b"
            app:strokeColor="#f7964f"
            app:strokeWidth="0.5dp"
            app:topRightRadius="5dp"
            app:topLeftRadius="10dp"
            app:bottomLeftRadius="5dp"
            app:bottomRightRadius="10dp"
            />
    </LinearLayout>

    <com.came.viewbguilib.ButtonBgUi
        android:layout_width="match_parent"
        android:layout_height="50dp"
        android:text="提交"
        android:textSize="18sp"
        android:textColor="#f7964f"
        android:clickable="true"
        android:layout_marginLeft="20dp"
        android:layout_marginRight="20dp"
        android:layout_marginTop="20dp"
        app:raoundRadius="5dp"
        app:strokeColor="#f7964f"
        app:strokeWidth="2dp"
        app:selectStrokeColor="#1fde94"
        android:background="#ffffff"
        />

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_marginLeft="20dp"
        android:layout_marginRight="20dp"
        android:layout_marginTop="20dp">

        <com.came.viewbguilib.ButtonBgUi
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="美妆"
            android:textSize="18sp"
            android:textColor="#f7964f"
            android:clickable="true"
            android:layout_marginLeft="30dp"
            android:padding="5dp"
            app:strokeWidth="2dp"
            app:strokeColor="#4be1c3"
            />

        <com.came.viewbguilib.ButtonBgUi
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_marginLeft="20dp"
            android:text="漫画"
            android:textSize="18sp"
            android:textColor="#f7964f"
            android:clickable="true"
            android:padding="5dp"
            app:strokeWidth="2dp"
            app:strokeColor="#4be1c3"
            app:raoundRadius="10dp"
            />
        <com.came.viewbguilib.ButtonBgUi
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="韩国电影"
            android:textSize="18sp"
            android:textColor="#f7964f"
            android:clickable="true"
            android:layout_marginLeft="20dp"
            android:padding="5dp"
            app:strokeWidth="2dp"
            app:strokeColor="#4be1c3"
            app:raoundRadius="20dp"
            app:defaultColor="#00000000"
            app:pressedColor="#fa734e"
            />
        <com.came.viewbguilib.ButtonBgUi
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="财经"
            android:textSize="18sp"
            android:textColor="#f7964f"
            android:clickable="true"
            android:layout_marginLeft="20dp"
            android:padding="5dp"
            app:strokeWidth="2dp"
            app:strokeColor="#4be1c3"
            app:topRightRadius="5dp"
            app:topLeftRadius="10dp"
            app:bottomLeftRadius="5dp"
            app:bottomRightRadius="10dp"
            />

    </LinearLayout>


</LinearLayout>

```
#####自定义属性说明
|属性|说明|
|----|----|
|strokeColor|默认边框的颜色|
|selectStrokeColor|选中边框的颜色|
|pressedColor|选中的背景色|
|defaultColor|默认的背景色|
|isRipple|是否设置水波纹效果|
|parameter|颜色变亮或变浅参数默认0.2|
|strokeWidth|边框的宽度|
|raoundRadius|圆角|
|topLeftRadius|左上角圆角|
|topRightRadius|右上角圆角|
|bottomLeftRadius|左下角圆角|
|bottomRightRadius|右下角圆角|

####注意事项》》》》》》》》
######1、如果不需要背景选择器，只需要不用设置defaultColor
```
 <com.came.viewbguilib.ButtonBgUi
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="美妆"
            android:textSize="18sp"
            android:textColor="#f7964f"
            android:clickable="true"
            android:layout_marginLeft="30dp"
            android:padding="5dp"
            app:strokeWidth="2dp"
            app:strokeColor="#4be1c3"
            />
```
######2、如果不设置pressedColor选中的颜色，会根据defaultColor默认的颜色判断选中的颜色是变亮或变暗
````
<com.came.viewbguilib.ButtonBgUi
            android:layout_width="0dp"
            android:layout_height="50dp"
            android:layout_marginRight="10dp"
            android:layout_weight="1"
            android:text="充值"
            android:textSize="18sp"
            android:textColor="#ffffff"
            android:clickable="true"
            app:defaultColor="#52adff"
            app:topRightRadius="25dp"
            app:bottomRightRadius="25dp"
            />
````
######3、如果不想在5.0+设备上有水波纹效果添加app:isRipple="false"

####如有什么问题，敬请提出，十分感谢！希望越来越好，谢谢！如果喜欢，还请点击start，喜欢支持一下了，谢谢O(∩_∩)O~
