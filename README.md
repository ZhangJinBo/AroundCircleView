# AroundCircleView
圆形图片 周围进度条 类似于音乐播放器的进度

 圆角显示图片  来自CircleImageView
 在基础上修改 让其可以周边动态显示进度

![](https://github.com/Daemon1993/AroundCircleView/blob/master/GIF.gif)


android studio gradle使用

    compile 'com.daemon:aroundcircleview2:1.0.1'
 
	<com.daemon.aroundcircleview.AroundCircleView
        android:id="@+id/acv_icon"
        android:layout_width="100dp"
        android:layout_height="100dp"
        android:layout_centerInParent="true"
        android:layout_gravity="center"
        android:src="@mipmap/pas"
        app:textColor="#147856"
        app:textSize="2dp" />
        
使用如下
view.setProgress(progress);
但是要在UI线程使用 内部用的Invalidate()而不是postInvalidate()  

