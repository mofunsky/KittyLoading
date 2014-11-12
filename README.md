KittyLoading
============

progress loading build by gradle

![image](https://github.com/reasonpun/KittyLoading/blob/master/library/images/img.jpeg)

xx_layout.xml

```
<com.reasono.kittyloading.ProgressWheel
        xmlns:ProgressWheel="http://schemas.android.com/apk/res-auto"
        android:id="@+id/progress_bar_two"
        android:layout_width="120dp"
        android:layout_height="120dp"
        ProgressWheel:barColor="#339BB9"
        ProgressWheel:barWidth="4dp"
        ProgressWheel:rimColor="#44000000"
        ProgressWheel:rimWidth="4dp"
        ProgressWheel:spinSpeed="3dp"
        ProgressWheel:text="click"
        ProgressWheel:textColor="#222222"
        ProgressWheel:textSize="14sp" />
```

xxActivity.java

```
findViewById(R.id.btnSetProgress).setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Button b = (Button) v;
                b.setText(i + "%");
                pwTwo.incrementProgressByHundredmark(i);

                if (i == 100) {
                    pwTwo.resetCount();
                    i = 0;
                }
                i += 10;
            }
        });

```