# Douyinliverecorder
抖音直播24小时无人值守录制工具


主要功能：


一、支持录制3种格式网址


1、主播主页：https://www.douyin.com/user/MS4wLjABAAAAltwgvfEGZhxPKpLrpVYxrAE-


2、电脑端直播链接：https://live.douyin.com/xxx


3、手机端分享链接：https://v.douyin.com/xxx


二、支持录制不同清晰度的flv或者hls直播流


1、FULL_HD1:蓝光 


2、HD1:超清 


3、ORIGION:原画 


4、SD1:标清 


5、SD2:高清


三、指定清晰度


1、正在直播的直播间可以在添加直播间的时候指定，也可以在添加完成后在网页界面的直播间设置里修改


2、添加直播间的时候未开播的直播间无法指定清晰度


四、录制生成的文件名前缀支持自定义


1、可用变量及说明


变量	            说明


.GirlName	      主播名称


.UniqueID	      抖音号


.PlatformCNName	平台中文名（如“抖音”）


.Now	          当前时间（可通过 now 函数格式化）


2、config.yml配置示例


out_put_tmpl: "{{ .Live.PlatformCNName }}/{{ .UniqueID }}/{{ now | date \"2006-01-02\" }}_{{ .GirlName | filenameFilter }}.flv"


out_put_tmpl: "{{ .GirlName | filenameFilter }}_{{ .UniqueID }}/[{{ now | date \"2006-01-02 15-04-05\" }}].flv"


