BadgeView for Android
=====================
我的成果（by Jerry Yin）：
    一。问题：此BadgeView 与 RadioButton 结合使用时会出现无法点击RadioButton和看不见按钮的情况？
        解决：1.在原位置的RadioGroup-RadioButton位置，以1:1的比例加上一层透明（android:background="#00000000"）的Button,用来加载此BadgeView; （无边框的button：style="?android:attr/borderlessButtonStyle"）
            ：2.请注意，如果你的RadioButton设置了点击事件的话，必须将 透明的button 设置为不可以点击的：具体为添加属性：（android:clickable="false"）； 
    二。在Android Studio环境使用的话，直接用badgeview.jar这个包就可以了；亲测可用。   
        
=====================
 原文：
An extended TextView that mimics the iOS Springboard 'badges'. It can be overlaid on any other item.

[Play Store Demo][1]



Setup
-----

In Eclipse, just import the library as an Android library project. Project > Clean to generate the binaries you need, like R.java, etc.
Then, just add BadgeView as a dependency to your existing project and you're good to go!

Sample Code
-----------

```java
BadgeView badge = new BadgeView(getActivity());
badge.setTargetView(myView);
badge.setBadgeCount(42);
```

Developed By
------------

* Stefan Jauker

License
-------

    Copyright 2013 Stefan Jauker
    
    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at
    
    http://www.apache.org/licenses/LICENSE-2.0
    
    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

[1]: https://play.google.com/store/apps/details?id=com.jauker.badgeview.example
