### zynq 7020

#### 1.架构

> * CPLD: 复杂可编程器件，基于`乘积项`的与或逻辑阵列；
> * FPGA: 现场可编程门阵列，基于查找表`LUT`的`CLB`阵列；

:star2: soc内部架构：![image-20260119195729181](D:\Workspace\Docs\FPGA\Xilinx\assets\image-20260119195729181.png)![image-20260119200319618](D:\Workspace\Docs\FPGA\Xilinx\assets\image-20260119200319618.png)![image-20260119200727818](D:\Workspace\Docs\FPGA\Xilinx\assets\image-20260119200727818.png)![image-20260119200914350](D:\Workspace\Docs\FPGA\Xilinx\assets\image-20260119200914350.png)

:star2: `PS`和`PL`互联交互相关接口如下图：![image-20260119202622502](D:\Workspace\Docs\FPGA\Xilinx\assets\image-20260119202622502.png)

:star2:  `AXI`总线相关：![image-20260119203229253](D:\Workspace\Docs\FPGA\Xilinx\assets\image-20260119203229253.png)

#### 2. 开发流程

![image-20260121193347206](D:\Workspace\Docs\FPGA\Xilinx\assets\image-20260121193347206.png)

##### 2.1 新建工程

![image-20260121193041622](D:\Workspace\Docs\FPGA\Xilinx\assets\image-20260121193041622.png)

![image-20260121193120905](D:\Workspace\Docs\FPGA\Xilinx\assets\image-20260121193120905.png)

##### 2.2 设计输入

##### 2.3 分析与综合

##### 2.4 时序约束

> :star2: 什么是时序约束：
>
> * 用来描述时序的具体要求如`输入输出延时`、`时钟频率`等；
> * 一般只对输入时钟做时序约束，输出时钟不做约束；
>
> :star2: 为什么要做时序约束：
>
> * 提高功能的稳定度，尤其是某些对硬件要求高的场合；
> * 由于寄存器资源布线资源都是随机分布的，不同布线长度不同；
>
> :star2: 哪些典型的场合需要时序约束：
>
> * 时钟频率较高的场景如`rgmii`，时钟频率为`125Mhz`双边沿采样；
> * 当资源比较紧张的时候可能优先满足布线要求而满足不了时钟的要求导致时钟无法达到预期或者无法稳定；
> * 遇到功能不能稳定使用的时候，优先考虑时序约束;
> * 时钟频率很高的传输如`PCIE`、`mipi`等频率比较高的场合；

















#### 5. VIA的使用&DEBUG方法