# OpenOCD工具箱
## OpenOCD介绍
OpenOCD是一个开源的调试软件，称之为世界上最强大的开源调试软件并不为过，经过数十年的开源社区的推动发展，当今其可调试数百种目标芯片，包括arm, mips, dsp, fpga, cpld等。支持多种调试接口，如cmsis-dap, jlink, stlink, usb-blaster等。  
## 脚本说明
以下是一些基于cmsis-dap接口的调试脚本，可以对目标芯片完成擦除、烧录、锁定等操作，当然您也可以自行修改脚本，以完成自己的定制需求。  
## 使用说明
**使用非常简单，无需安装任何额外软件，以及额外的配置，您只需将本仓库下载下来，双击其中脚本即可运行，实际使用会比图形界面操作更加高效，也更加强大**   
## 脚本说明
```
#attach到cpu上，您可双击此脚本，观察输出，以确认仿真器和是否和目标板正确连接
attach.bat

# dump出目标芯片中的flash，不同目标芯片由于flash空间不同，或许您需要手动编辑文件修改其中的flash空间大小
flash_dump.bat

# 擦除目标芯片flash
flash_erase.bat

# 将当前目录下的flash_image.bin写入到目标芯片中，您可自行修改其中的路径及文件名
flash_write.bat

# 对目标芯片锁定，即增加读保护，加上读保护之后，无法从调试接口访问flash空间，若执行解锁操作，则芯片内部逻辑会擦除所有flash数据
lock.bat

# 解锁目标芯片，会擦除所有flash数据
unlock.bat
```
## 支持平台
当前支持如下平台的操作  
- **stm32f0x**  
- **stm32f1x**  

若您有需求，请在本仓库的issue中上报新平台，脚本会持续更新。
