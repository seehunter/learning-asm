# 汇编语言（第2版）-王爽，所有源码和练习

    1. 计算机基本组成：cpu+外部总线+主存储器+其他外设ram+其他外设rom
    2. 寻址能力  数据总线位数（宽度） 内部总线（cpu内部，算术逻辑单元） 外部总线（cpu与外部设备）
    3. 地址总线寻址
    4. 数据总线拿送数据
    5. 控制总线控制读写
    6. 寄存器分类
        通用寄存器
        段寄存器：cs（代码段寄存器） ds（数据段寄存器） ss（堆栈段寄存器，支持堆栈操作 关联pop push ） es（附加段寄存器）
    7. 指令相关：cs+ip   代码段寄存器（取基地址）+指令寄存器（取偏移地址）
        物理地址=16x段地址+偏移地址（通过地址转换器+输入输出控制电路）
        phisicaddr=sa16+ea （通过地址转换器+输入输出控制电路）
    8. 指令载入过程：
        cpu（（ax，bx...）（其他部件），(cs,ip)=>地址加分器=》输入输出设备=》（20位地址总线，数据总线） 

## debug 命令

        进入dos系统 输入debug.exe
        执行单元查看：  r
        向执行单的寄存器写入数据：（先要运行 r命令） r ax(ah,al) bx(bh,bl) cx(ch,cl) dx(dh,dl) cs ip
        查看内存数据：d sa:ea(段地址：偏移地址)
        查看当前要执行的指令（要运行的程序的指令）对应汇编指令：u
        更改要执行的代码段：1.r cs (接着输入段地址) 2.r ip （接着输入偏移地址）
        向指定内存写入要执行的机器指令： e sa:ea(段地址：偏移地址)
        向指定内存写入要执行的汇编指令： a sa:ea(段地址：移动地址) 直接使用a命令直接向当前cs段写入
        一条一条执行指令：t

## 数据寻址

    指定数据段  mov bx,addr mov ds,bx mov ax,[0]  使用[]寻址
       1. 指定段地址（段地址不能使用立即数寻址）
       2. 使用[]指定偏移地址

    move,add,sub





