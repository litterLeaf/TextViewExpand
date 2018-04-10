# TextViewExpand
减少布局的嵌套只要一个控件

![image](https://github.com/litterLeaf/TextViewExpand/blob/master/show/result.jpg) 

以下面的第二行为例 

未用新的自定义控件前：

    <RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    	xmlns:app="http://schemas.android.com/apk/res-auto"
    	xmlns:tools="http://schemas.android.com/tools"
    	android:layout_width="match_parent"
    	android:layout_height="60dp"
    	android:orientation="vertical">
	
		<TextView
            android:id="@+id/textView"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_centerVertical="true"
            android:layout_gravity="center_vertical"
            android:layout_marginLeft="20dp"
            android:layout_marginStart="20dp"
            android:layout_alignParentLeft="true"
            android:text="文字1" />

		<TextView
            android:id="@+id/delete"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_alignParentRight="true"
            android:layout_centerVertical="true"
            android:layout_marginRight="15dp"
            android:text="文字2" />

     </RelativeLayout>

现在：
	
	<com.riven.library.TextViewExpand
        android:layout_width="match_parent"
        android:layout_height="60dp"
        app:eLeftTextString="文字1"
        app:eRightTextString="文字2"
        />
	
你还在为布局嵌套太多头疼么，调用此控件就可以轻松拜托此现象，所以赶紧起来吧！
## 引用方法（gradle）
Add it in your root build.gradle at the end of repositories:


    allprojects {
		  repositories {
			  ...
			  maven { url 'https://jitpack.io' }
		  }
	  }
    
Add the dependency
  
    dependencies {
	        compile 'com.github.litterLeaf:TextViewExpand:1.0.1'
	  }
   
   ## 欢迎大家使用，有什么问题可以联系我 邮箱 598678782@qq.com
