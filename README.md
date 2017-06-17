# hfs_for_oss
HTTP File Server for AliYun OSS  
A modern HTTP File Server for oss@aliyun.  
一款现代化的http文件服务器，为阿里云OSS对象存储服务提供支持。 
  
SDK由[aliyun-oss-php-sdk](https://help.aliyun.com/document_detail/32101.html?spm=5176.doc52834.6.753.ihtpJC)-2.2.4提供，主题由[h5ai](https://larsjung.de/h5ai/)提供。

## 预览 & 下载/Demo & Download
* 预览：http://file.oovoo.site/
* 下载：https://github.com/YuXuan220/hfs_for_oss/releases

## 部署/Build
* 环境要求：  
PHP 5.5及以上（没有证据表明程序无法在PHP5.5以下正常运行）
* 文件结构：
```
/
├──aliyun-oss-php-sdk-2.2.4/	--SDK目录
  ├──src/
    ├──...
  ├──autoload.php
  └──common.php
├──h5ai/	--h5目录
  ├──css/
    ├──style.css  --可自定义的css
  ├──images/
    ├──...
  ├──js/
    ├──...
├──config.php	--配置文件
├──get_files.php	--listObjects(), 获取文件列表
└──index.php	--首页
```
* 配置：   
~~~php
/config.php: 
<?php  
final class Config  
{  
	const OSS_ACCESS_ID = '';   //Access Key ID  
	const OSS_ACCESS_KEY = '';    //Access Key Secret  
	const OSS_ENDPOINT = ''; //OSS EndPoint (e.g. http://oss-cn-shanghai.aliyuncs.com)  
	const OSS_BUCKET = ''; //OSS Bucket Name  
}  
$site = '' ;   //Site Name  
$footer = '';   //Footer, Stats Code Supported  
$stats = true ;    //Display how long listObjects() takes? (true/false)  
~~~

## 后续可能的改动/Preview
```
[修复] 路径层级到某一数量后上一级文件夹名称显示不正常
[新增] 输出item的大小
[新增] 上方crumbbar路径多级显示（逐个操作字符串滤出path里的每一级路径真的很麻烦。。能用"../"就好了啊我也很绝望啊）
[新增] 简单的object管理功能（上传，重命名等）
[永远不可能有的功能\]（不好意思我懒，嘴角挂着和善的微笑）） 文件列表排序
```

## 更新日志/ChangeLog
```
version 1.0.0 2017-06-17
	破壳。
```

## 开源协议/License
（虽然我很想用WTFPL啊，（笑~））
```
The MIT License (MIT) 
 
Copyright (c) 2016 Lars Jung (https://larsjung.de)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
```