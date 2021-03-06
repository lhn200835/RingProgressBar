# RingProgressBar

一个简单实现的自定义圆环进度条,可使用于文件的上传下载图片加载等地方.


## 截图

![](https://github.com/HotBitmapGG/RingProgressBar/blob/master/pic/ring.gif?raw=true)

# 导入项目
 
 Step 1. Add the JitPack repository to your build file
 Add it in your root build.gradle at the end of repositories:

	allprojects {
		repositories {
			...
			maven { url "https://jitpack.io" }
		}
	}



Step 2. Add the dependency

	dependencies {
	         compile 'com.github.HotBitmapGG:RingProgressBar:V1.2.1'
	}

## 使用说明

* 自定义属性介绍

name | format | 说明
-----|------|----
ringColor    | color    | 圆环颜色
ringProgressColor   | color     | 进度颜色
ringWidth    | dimension    | 圆环进度宽度
textColor   | color   | 文本颜色
textSize    | dimension    | 文本大小
max    | integer    | 最大进度值
textIsShow    | boolean    | 是否显示文本
style    | STROKE& FILL   | 圆环进度样式


## 用法

* 1.在XML中

 *  app:max="100"
 *  app:ringColor="@color/colorPrimary"
 *  app:ringProgressColor="@color/colorPrimaryDark"
 *  app:ringWidth="4dp"
 *  app:style="STROKE"
 *  app:textColor="@color/colorPrimary"
 *  app:textIsShow="true"
 *  app:textSize="16sp"

* 2.代码中

  mRingProgressBar = (RingProgressBar) findViewById(R.id.progress_bar);

  //设置进度条的进度值
  mRingProgressBar.setProgress(progress);
  </p>
  mRingProgressBar.setOnProgressListener(new RingProgressBar.OnProgressListener()
  {

    @Override
     public void progressToComplete()
     {
         // 进度达到最大值时回调 默认max进度值为100
         Toast.makeText(MainActivity.this, "完成", Toast.LENGTH_SHORT).show();
     }
  });


## Tips

 * 增加了完成后一个对勾显示的动画效果,但是不知道这个有没有实际的用途,所以代码中注释掉了,有需要的同学可以打开注释使用.

## Other

  * 知了日报客户端: https://github.com/HotBitmapGG/RxZhiHu

  * 高仿BiliBili客户端: https://github.com/HotBitmapGG/OhMyBiliBili

  * Gank.IO客户端: https://github.com/HotBitmapGG/StudyProject

  * 妹子福利App: https://github.com/HotBitmapGG/MoeQuest

  * 圆环进度条:https://github.com/HotBitmapGG/RingProgressBar

  * 安卓学习代码练习:https://github.com/HotBitmapGG/AndroidEveryDayPractice
  
  * 轻量级的RecycleViewAdapter辅助类库 :https://github.com/HotBitmapGG/EasyRecycleAdapterHelper

## License

 Copyright 2016 HotBitmapGG

 Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

 http://www.apache.org/licenses/LICENSE-2.0

 Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.




