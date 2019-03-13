#  实验二_Android布局 
1.  利用线性布局实现如下界面：
![first](https://wx2.sinaimg.cn/mw690/e9e52fd7gy1g113bsf1vvj20gk06adg1.jpg)
    1. 关键代码：
    ```xml
    <LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:orientation="vertical"> 
        <!--  first line --> 
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content">
        <Button
            android:id="@+id/button"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:text="one,one" />
        <Button
            android:id="@+id/button2"
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="2"
            android:text="one,two" />
        <Button
            android:id="@+id/button3"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:text="one,three" />
        <Button
            android:id="@+id/button4"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:text="one,four" />
        /LinearLayout>
        <!--  second line -->
        <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content">
        <Button
            android:id="@+id/button5"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:text="two,one" />
        <Button
            android:id="@+id/button6"
            android:layout_width="0dp"
            android:layout_height="match_parent"
            android:layout_weight="2"
            android:text="two,two" />
        <Button
            android:id="@+id/button7"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:text="two,three" />
        <Button
            android:id="@+id/button8"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:text="two,four" />
        </LinearLayout>
        <!--  third line -->
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content">
            <Button
                android:id="@+id/button9"
                android:layout_width="0dp"
                android:layout_height="wrap_content"
                android:layout_weight="1.1"
                android:text="three,one" />
            <Button
                android:id="@+id/button10"
                android:layout_width="0dp"
                android:layout_height="match_parent"
                android:layout_weight="1.1"
                android:text="three,two" />
            <Button
                android:id="@+id/button11"
                android:layout_width="0dp"
                android:layout_height="wrap_content"
                android:layout_weight="1.1"
                android:text="three,three" />
            <Button
                android:id="@+id/button12"
                android:layout_width="0dp"
                android:layout_height="wrap_content"
                android:layout_weight="1.1"
                android:text="three,four" />
        </LinearLayout>
        <!--  fourth line -->
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content">
            <Button
                android:id="@+id/button13"
                android:layout_width="0dp"
                android:layout_height="wrap_content"
                android:layout_weight="1"
                android:text="four,one" />
            <Button
                android:id="@+id/button14"
                android:layout_width="0dp"
                android:layout_height="match_parent"
                android:layout_weight="2"
                android:text="four,two" />
            <Button
                android:id="@+id/button15"
                android:layout_width="0dp"
                android:layout_height="wrap_content"
                android:layout_weight="1"
                android:text="four,three" />
            <Button
                android:id="@+id/button16"
                android:layout_width="0dp"
                android:layout_height="wrap_content"
                android:layout_weight="1"
                android:text="four,four" />
        </LinearLayout>
    </LinearLayout>
    ```
    1. 模拟器截图：![first ans](https://wx1.sinaimg.cn/mw690/e9e52fd7gy1g1138t1xtzj20de0nb0wa.jpg)

1. 利用ConstraintLayout实现如下
![second](https://wx2.sinaimg.cn/mw690/e9e52fd7gy1g113bsjv3uj20e308fjrb.jpg)
    1. 关键代码：
    1. 模拟器截图：
1.  利用表格布局实现如下界：

![third](https://wx2.sinaimg.cn/mw690/e9e52fd7gy1g113bsnz0xj206y09mweb.jpg)
    
    1. 关键代码：
    1. 模拟器截图：