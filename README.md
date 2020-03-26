# UserAgent for Typecho

Typecho 插件，用于在评论区显示用户使用的操作系统、浏览器信息及对应图标。

## 使用说明

1. 解压后修改文件夹名为 UserAgent，将插件上传至网站目录的 `/usr/plugins` 下
2. 在 Typecho 后台「插件管理」处启用插件
3. 在需要显示的地方插入以下代码：

```php
<?php UserAgent_Plugin::render($comments->agent); ?>
```
若显示图标为问号则改为：
```php
<?php UserAgent_Plugin::render($this->agent); ?>
```
若为mirages主题则放在/lib/Comments.php的123行，即
  ```
  $singleCommentOptions->afterAuthor(); ?></cite>
    <?php UserAgent_Plugin::render($this->agent); ?>
  </div>
  ```
## 更新日志
- v1..0&emsp;（2019/03/27）添加了基于Chromium内核的新版Edge浏览器图标，替换了部分颜色过饱和的图标。
## 致谢

### 原项目

本项目基于 [hakula139](https://github.com/hakula139) 的项目 [UserAgent for Typecho](https://github.com/hakula139/UserAgent-for-Typecho)，在此感谢。

新版Edge浏览器发布有一段时间了，很少见到评论区UA图标用新版的，最多见到的是旧版图标新版的版本号，好在这个插件改动起来相对容易，还加入了自己使用的主题启用插件的方法，算是个备忘录。

### Iconfont
### wikimedia

> [Iconfont](https://www.iconfont.cn) - 阿里巴巴矢量图标库<br />
>[wikimedia](https://commons.wikimedia.org/wiki/File:Microsoft_Edge_logo.svg) - Microsoft Edge logo

新版Edge浏览器图标由wikimedia提供，其余操作系统、浏览器图标均使用 Iconfont 提供的 SVG 矢量图标，在此感谢两个平台。

## 问题反馈

本人根本没学过一门语言，全靠一点英语基础和感觉改代码，只是改了自己用，放在这里备份托管一下。

所以建议到原作者[个人博客](https://hakula.xyz/project/ua_typecho.html)留言，或者通过[邮箱](mailto:i@hakula.xyz)联系他。

