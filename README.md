# RotaryBallLoadingProgressDialog1.0
两个小球旋转的动画，一个清新的进度条

##效果图
![image](https://github.com/dalong982242260/RotaryBallLoadingProgressDialog1.0/blob/master/screenshot/twoballrotationprogressbar.gif)

##Requirements

---

Min Sdk Version:14

因为Android2.x的用户量很少了，没有必要再兼容了，这里没有使用nineoldandroids这个兼容库来做属性动画


##How to use

    dependencies {
             ...
             compile 'com.dalong:rotaryballview:1.0.0'
    }



##Proguard


因为这里使用了@Keep注解来防止混淆，目前Gradle还没有这个混淆插件，所以要手动开启一下
在app/proguard-rules.pro里面添加

\#手动启用support keep注解

\#http://tools.android.com/tech-docs/support-annotations

-keep,allowobfuscation @interface android.support.annotation.Keep

-keep @android.support.annotation.Keep class *

-keepclassmembers class * {

    @android.support.annotation.Keep *;
}



