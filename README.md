# LearnAndroid
收集平常用到的一些命令~

*********************************************
Wechat：18305165010
CSDN  ：https://blog.csdn.net/ctrl_qun


1、发送广播：
am broadcast 后面为key 加参数.具体：
[-a <ACTION>]
[-d <DATA_URI>]
[-t <MIME_TYPE>] 
[-c <CATEGORY> [-c <CATEGORY>] ...] 
[-e|--es <EXTRA_KEY> <EXTRA_STRING_VALUE> ...] 
[--ez <EXTRA_KEY> <EXTRA_BOOLEAN_VALUE> ...] 
[-e|--ei <EXTRA_KEY> <EXTRA_INT_VALUE> ...] 
[-n <COMPONENT>]
[-f <FLAGS>] [<URI>]

-a  后面为 action
--es 为 EXTRA_KEY

adb shell am broadcast -a action.com.custom.broadcast.quit  --es package "com.test.broadcast"
转换为代码为:
Intent intent = new Intent("action.com.custom.broadcast.quit");
intent.putExtra("package","com.test.broadcast");

2、启动activity
# am start -n 包(package)名/包名.活动(activity)名称
或者am start -n 包(package)名/.活动(activity)名称
启动的方法可以从每个应用的AndroidManifest.xml的文件中得到
Music （音乐）的启动方法为：
# am start -n com.android.music/com.android.music.MusicBrowserActivity
或者am start -n com.android.music/.MusicBrowserActivity