# Android-Img2Ascii
[![Android Arsenal](https://img.shields.io/badge/Android%20Arsenal-Img2Ascii-red.svg?style=flat)](https://android-arsenal.com/details/1/6393)
[![Release](https://jitpack.io/v/bachors/Android-Img2Ascii.svg)](https://jitpack.io/#bachors/Android-Img2Ascii)

Convert image to ascii.

Gradle
------
```
allprojects {
   repositories {
      ...
      maven { url 'https://jitpack.io' }
   }
}
```
```
dependencies {
    ...
    compile 'com.github.bachors:Android-Img2Ascii:1.1'
}
```

Usage
-----
```java
...

// bitmap
Bitmap image = BitmapFactory.decodeResource(getResources(), R.drawable.image);
// Bitmap image = BitmapFactory.decodeFile(filename);

new Img2Ascii()
   .bitmap(image)
   .quality(3) // 1 - 5
   //.color(true)
   .convert(new Img2Ascii.Listener() {
      @Override
      public void onProgress(int percentage) {
         textView.setText(String.valueOf(percentage) + " %");
      }
      @Override
      public void onResponse(Spannable text) {
         textView.setText(text);
      }
   });
```

Demo
-----
![demo](https://i.imgflip.com/29wvub.gif)
