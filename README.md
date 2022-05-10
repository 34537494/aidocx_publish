# `wpsjs`的发布与部署

通过`wpsjs build`指令，先将项目编译

使用`wpsjs publish`指令，配置一个安装界面，其地址为服务器地址，可以通过[本地创建服务器](https://www.cnblogs.com/wangxiayun/p/9851325.html)，配置一个本地路径，并添加7z的下载格式到服务器

![image-20220509100035776](image\image-20220509100035776.png)

![image-20220509100109152](image\image-20220509100109152.png)

将路径输入到指令中

![image-20220509094313892](image\image-20220509094313892.png)

然后将`wps-addon-build`（由`wpsjs build`指令创建）的压缩包放置在刚刚配置的路径中

![image-20220509124240958](image\image-20220509124240958.png)

并检查刚刚配置的路径+压缩包名（如aidocx.7z）在浏览器中是否可以发起一个下载的弹窗，如果可以就继续

运行win+r，输入`%appdata%`进入`appdata`的文件夹，找到`kingsoft/wps/jsaddons`，里面有个`jsaddons.xml`，添加`jsaddon`，名称和版本号要跟`wps-addon-build`解压出来的名字对应，`name+"_"+version`即可，`url`为之前配置的压缩包放置的位置（或许也可以是本地路径，我没有尝试）

通过`wps-addon-publish`（由`wpsjs publish`指令创建）中的publish.html进入加载项配置页，点击安装即可

![image-20220509095948214](image\image-20220509095948214.png)





reference：

https://www.kdocs.cn/l/cASCu9B0G

https://www.kdocs.cn/l/cBk8tsBIf
