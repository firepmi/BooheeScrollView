# BooheeScrollView

Imitate the effect of mint food library

# ScreenShot


![image](https://github.com/firepmi/BooheeScrollView/blob/master/screenshot/screen.gif)


# Usage
### Step 1
   Implement a similar layout in the layout file    
    
    <com.zzt.library.BooheeScrollView
        android:layout_alignParentBottom="true"
        android:id="@+id/horizon"
        android:overScrollMode="never"
        android:layout_width="match_parent"
        android:layout_height="wrap_content">
        <com.zzt.library.BuildLayerLinearLayout
            android:id="@+id/linear"
            android:orientation="horizontal"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content">
        </com.zzt.library.BuildLayerLinearLayout>
    </com.zzt.library.BooheeScrollView>
    
### Step 2
   Create the content to be displayed according to the appropriate size and add it to buildLayerLinearLayout
   
        BezelImageView imageView2 = new BezelImageView(this);
        imageView2.setLayoutParams(new LinearLayout.LayoutParams(width, height));
        buildLayerLinearLayout.addView(imageView2);
        imageView2.setImageBitmap(decodeSampledBitmapFromResource(getResources(),  R.drawable.pic2, width, height));
        imageView2.setMaskDrawable(getResources().getDrawable(R.drawable.roundrect));
        
### Step 3
   Add the content to be rotated here
    
    booheeScrollView.setChildViews(new View[]{
        cardView1, imageView1,imageView2, imageView3,
        imageView4, imageView5, imageView6, imageView7});
        

