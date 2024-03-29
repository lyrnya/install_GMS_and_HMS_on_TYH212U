# 在天翼1号2022上安装GMS和HMS(非面具模块)

# 为什么不使用面具刷入 GMS 和 HMS 模块？
- 此方法能够在狐狸面具SuList白名单下正常运行，shamiko白名单估计也可以
- 模块无法在白名单下正常工作
  - 官方面具 26400 开启 shamiko 白名单，GMS 和 HMS 无法正常运行
  - 狐狸面具 26400 开启 SuList 白名单，GMS 和 HMS 无法正常运行
- 尝试手动安装 HMSCore.apk 后 HMS 正常运行(依旧还是系统应用)，理论上手动安装 GMS 的这几个 apk 也能解决问题，但是在安装 GoogleServicesFramework.apk 时提示安装包无效无法安装

# 安装教程

### 1.面具刷入Magic Overlayfs模块
- Overlayfs：[下载链接](https://github.com/HuskyDG/magic_overlayfs/releases/download/v3.2.2/magisk-overlayfs-release.zip)
![刷入模块然后重启](https://github.com/boxhz/install_GMS_and_HMS_on_TYH212U/blob/master/Picture/magiskoverlayfs.png)

### 2.下载 GMS 和 HMS

- GMS: [下载链接](https://mirror.ghproxy.com/https://github.com/boxhz/install_GMS_and_HMS_on_TYH212U/releases/download/V1/GMS.zip) []() Weeb GApps 4.1.8
- HMS: [下载链接](https://mirror.ghproxy.com/https://github.com/boxhz/install_GMS_and_HMS_on_TYH212U/releases/download/V1/HMS.zip) []() HMS Core 6.10

### 3.解压压缩包，将文件复制到/system/product/下对应的目录

- 将压缩包app文件夹里的文件复制到/system/product/app/目录下
- 将压缩包etc文件夹里的文件复制到/system/product/etc/目录下
- 将压缩包framework文件夹里的文件复制到/system/product/framework/目录下
- 将压缩包priv-app文件夹里的文件复制到/system/product/priv-app/目录下

![将文件复制到对应的目录](https://github.com/boxhz/install_GMS_and_HMS_on_TYH212U/blob/master/Picture/product.png)

### 4.设置新增文件夹及文件权限

- 文件夹设置755权限 所有者和用户组改为root
![设置文件夹权限](https://github.com/boxhz/install_GMS_and_HMS_on_TYH212U/blob/master/Picture/755.png)
- 文件设置644权限 所有者和用户组改为root
![设置文件权限](https://github.com/boxhz/install_GMS_and_HMS_on_TYH212U/blob/master/Picture/644.png)

### 5.重启
- 重启后在设置-辅助功能打开谷歌基础服务然后即可在设置-账号和同步里面看到Google账号和华为账号
