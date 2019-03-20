#  实验二_Android布局 
1.  利用线性布局实现如下界面：

    ![first](https://wx2.sinaimg.cn/mw690/e9e52fd7gy1g113bsf1vvj20gk06adg1.jpg)

    1. 关键代码：
    ```xml
    <?xml version="1.0" encoding="utf-8"?>
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
    1. 模拟器截图：
    
    ![first ans](https://wx1.sinaimg.cn/mw690/e9e52fd7gy1g1138t1xtzj20de0nb0wa.jpg)

1. 利用ConstraintLayout实现如下
    
    ![second](https://wx2.sinaimg.cn/mw690/e9e52fd7gy1g113bsjv3uj20e308fjrb.jpg)

    1. 关键代码：

    ```xml
    <?xml version="1.0" encoding="utf-8"?>
    <android.support.constraint.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/linearLayout"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#000000">
    <TextView
        android:id="@+id/textView"
        android:layout_width="90dp"
        android:layout_height="66dp"
        android:layout_marginStart="7dp"
        android:layout_marginLeft="7dp"
        android:background="#fF0000"
        android:gravity="center"
        android:text="RED"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />
    <TextView
        android:id="@+id/textView11"
        android:layout_width="123dp"
        android:layout_height="66dp"
        android:layout_marginEnd="7dp"
        android:layout_marginRight="7dp"
        android:background="#ffff00"
        android:gravity="center"
        android:text="YELLOW"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintTop_toTopOf="parent" />
    <TextView
        android:id="@+id/textView12"
        android:layout_width="123dp"
        android:layout_height="66dp"
        android:layout_marginStart="8dp"
        android:layout_marginLeft="8dp"
        android:layout_marginEnd="8dp"
        android:layout_marginRight="8dp"
        android:background="#FF9900"
        android:gravity="center"
        android:text="ORANGE"
        app:layout_constraintEnd_toStartOf="@+id/textView11"
        app:layout_constraintHorizontal_bias="0.598"
        app:layout_constraintStart_toEndOf="@+id/textView"
        app:layout_constraintTop_toTopOf="parent" />
    <TextView
        android:id="@+id/textView13"
        android:layout_width="517dp"
        android:layout_height="49dp"
        android:layout_marginStart="7dp"
        android:layout_marginLeft="7dp"
        android:layout_marginTop="8dp"
        android:layout_marginEnd="7dp"
        android:layout_marginRight="7dp"
        android:layout_marginBottom="7dp"
        android:background="#CC66CC"
        android:gravity="center"
        android:text="VIOLET"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.0"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="1.0" />
    <TextView
        android:id="@+id/textView14"
        android:layout_width="98dp"
        android:layout_height="64dp"
        android:layout_marginStart="112dp"
        android:layout_marginLeft="112dp"
        android:layout_marginTop="8dp"
        android:layout_marginBottom="8dp"
        android:background="#33ff00"
        android:gravity="center"
        android:text="GREEN"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.525" />
    <TextView
        android:id="@+id/textView15"
        android:layout_width="83dp"
        android:layout_height="64dp"
        android:layout_marginStart="8dp"
        android:layout_marginLeft="8dp"
        android:layout_marginTop="8dp"
        android:layout_marginEnd="8dp"
        android:layout_marginRight="8dp"
        android:layout_marginBottom="8dp"
        android:background="#0033CC"
        android:gravity="center"
        android:text="BLUE"
        android:textColor="#ffffff"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toStartOf="@+id/textView16"
        app:layout_constraintHorizontal_bias="0.0"
        app:layout_constraintStart_toEndOf="@+id/textView14"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.528" />
    <TextView
        android:id="@+id/textView16"
        android:layout_width="98dp"
        android:layout_height="64dp"
        android:layout_marginTop="8dp"
        android:layout_marginEnd="124dp"
        android:layout_marginRight="124dp"
        android:layout_marginBottom="8dp"
        android:background="#660099"
        android:gravity="center"
        android:text="INDIGO"
        android:textColor="#ffffff"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.525" />
    </android.support.constraint.ConstraintLayout>
    ```
    1. 模拟器截图：

    ![在这里插入图片描述](https://img-blog.csdnimg.cn/20190313202328736.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjQ3OTEzNA==,size_16,color_FFFFFF,t_70)

1.  利用表格布局实现如下界：

    ![third](https://wx2.sinaimg.cn/mw690/e9e52fd7gy1g113bsnz0xj206y09mweb.jpg)

    1. 关键代码：

    ```xml
    <?xml version="1.0" encoding="utf-8"?>
    <TableLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:stretchColumns="1">
    <TableRow>
        <TextView
            android:id="@+id/textView1"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_column="0"
            android:gravity="center"
            android:text="Open..." />
        <TextView
            android:id="@+id/textView2"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_column="3"
            android:gravity="right"
            android:text="Ctrl+O" />
    </TableRow>
    <TableRow>
        <TextView
            android:id="@+id/textView3"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_column="0"
            android:gravity="center"
            android:text="Save..." />
        <TextView
            android:id="@+id/textView4"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_column="3"
            android:gravity="right"
            android:text="Ctrl+S" />
    </TableRow>
    <TableRow>
        <TextView
            android:id="@+id/textView5"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_column="0"
            android:gravity="center"
            android:text="Save As..." />
        <TextView
            android:id="@+id/textView6"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_column="3"
            android:gravity="right"
            android:text="Ctrl+shift+S" />
    </TableRow>
    <!--横线-->
    <View
        android:layout_height="2px"
        android:layout_width="match_parent"
        android:background="#000000" />
    <TableRow>
        <TextView
            android:id="@+id/textView7"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_column="0"
            android:gravity="center"
            android:text="X Import..." />
    </TableRow>
    <TableRow>
        <TextView
            android:id="@+id/textView8"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_column="0"
            android:gravity="center"
            android:text="X Export..." />
        <TextView
            android:id="@+id/textView9"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_column="3"
            android:gravity="right"
            android:text="Ctrl+E" />
    </TableRow>
    <View
        android:layout_height="2px"
        android:layout_width="match_parent"
        android:background="#000000" />
    <TableRow>
        <TextView
            android:id="@+id/textView10"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_column="0"
            android:gravity="center"
            android:text="Quit" />
        </TableRow>
    </TableLayout>
    ```
    1. 模拟器截图：

    ![third ans](https://img-blog.csdnimg.cn/20190313191256951.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjQ3OTEzNA==,size_16,color_FFFFFF,t_70)

1. 模拟器主界面（点击按钮跳转界面）

    ![在这里插入图片描述](https://img-blog.csdnimg.cn/20190320114950425.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80MjQ3OTEzNA==,size_16,color_FFFFFF,t_70)
    
    1. 核心代码

    index.xml

    ```xml
    <LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical">
    <Button
        android:id="@+id/button1"
        android:layout_width="148dp"
        android:layout_height="30dp"
        android:layout_gravity="center"
        android:layout_marginTop="10dp"
        android:layout_marginBottom="10dp"
        android:layout_weight="1"
        android:text="LinearLayout" />
    <Button
        android:id="@+id/button2"
        android:layout_width="150dp"
        android:layout_height="21dp"
        android:layout_gravity="center"
        android:layout_marginTop="10dp"
        android:layout_marginBottom="10dp"
        android:layout_weight="1"
        android:text="ConstraintLayout" />
    <Button
        android:id="@+id/button3"
        android:layout_width="154dp"
        android:layout_height="29dp"
        android:layout_gravity="center"
        android:layout_marginTop="10dp"
        android:layout_marginBottom="10dp"
        android:layout_weight="1"
        android:text="TableLayout" />
    </LinearLayout> 
    ```
    MainAcitvity.java
    ```java
    import android.app.Activity;
    import android.os.Bundle;
    import android.widget.Button;
    import android.view.View;
    import android.content.Intent;

    public class MainActivity extends Activity {
        private Button button1,button2,button3;
        @Override
        protected void onCreate(Bundle savedInstanceState) {
            super.onCreate(savedInstanceState);
            setContentView(R.layout.index);
            button2 = (Button) findViewById(R.id.button2);//id后面为上方button的id
            button2.setOnClickListener(new View.OnClickListener() {
                @Override
                public void onClick(View view) {
                    Intent intent=new Intent(MainActivity.this,SecondActivity.class);
                    startActivity(intent);
                }
            });
            button1 = (Button) findViewById(R.id.button1);//id后面为上方button的id
            button1.setOnClickListener(new View.OnClickListener() {
                @Override
                public void onClick(View view) {
                    Intent intent=new Intent(MainActivity.this,FirstActivity.class);
                    startActivity(intent);
                }
            });
            button3 = (Button) findViewById(R.id.button3);//id后面为上方button的id
            button3.setOnClickListener(new View.OnClickListener() {
                @Override
                public void onClick(View view) {
                    Intent intent=new Intent(MainActivity.this,ThirdActivity.class);
                    startActivity(intent);
                }
            });
        }
    }
    ```