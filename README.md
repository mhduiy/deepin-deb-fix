## Deepin Deb Fix

由于部分商店应用的启动脚本未添加shebang，systemd无法执行启动脚本造成应用启动失败，经过讨论后，现准备通过执行一个脚本将有问题的启动脚本手动加上shebang，并将修补过的启动脚本和desktop文件作为源码放在deepin-deb-fix中，安装此包后会将修补目录添加到XDG_DATA_DIRS环境变量中，即可在启动应用时执行修补过的启动脚本，达到修复问题的目的

## 更新应用步骤

1. 执行项目根目录的checkDeb.sh脚本
2. 上传仓库即可

注：其他架构的包暂无问题，目前只排查amd64的包;脚本执行时间较长，执行时会在同级目录生成check.log日志文件，部分warning级别的日志表示可能需要手动干预

## License

Deepin Deb Fix is licensed under [GPL-3.0-or-later](LICENSE).
