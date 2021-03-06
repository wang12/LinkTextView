# LinkTextView
Made TextView with **ClickableSpan** more easy

[ ![Download](https://api.bintray.com/packages/rookieboy/maven/linktextview/images/download.svg?version=0.0.1) ](https://bintray.com/rookieboy/maven/linktextview/0.0.1/link)

<img src="https://raw.githubusercontent.com/REBOOTERS/Images/master/LinkTextView/art.gif"/>



## Gradle 

```groovy
	 implementation "com.reoobter:linktextview:0.0.1"
```

## Usage

```kotlin
// the content should be set for TextView
val android = getString(R.string.text_android_baike) 
// Array to define all clickable words
val androidRules = arrayOf("Linux","操作系统","移动设备","智能手机","平板电脑","开放手机联盟") 

Linker.Builder()
    .content(android)
    .textView(text_view_1)
    .links(androidRules)
    .linkColor(ContextCompat.getColor(this,R.color.link))
    .addOnLinkClickListener(onLinkClickListener)
    .apply()

private val onLinkClickListener = object:OnLinkClickListener{
    override fun onClick(view: View, content: String) {
        Toast.makeText(mContext, "clicked link is : $content", Toast.LENGTH_SHORT).show()
    }
}

```

## API 

 method | function | must invocation| defaultValue
 -------|  --------| ---------|------
|conent|content for TextView|yes| none|
|textview|TextView used for set clickable words|yes| none|
|links|String/Array<String>/List<String> to define clickable words |no| none|
|linkColor|Color for clickable word|no| Color.Black|
|shouldShowUnderLine|whether to show under for clickable word|no| false|
|addOnLinkClickListener|add a listener will callback once click the link word|no| null|
|apply|apply the function|yes| none|


## TODO

- [ ] different color for links 


## License 

---------------------

    Copyright 2019 REBOOTERS

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.


