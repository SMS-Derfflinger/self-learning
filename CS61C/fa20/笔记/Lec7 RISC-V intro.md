# RISC-V introduction

* 计算机系统抽象层：
![alt text](image.png)

# Register

汇编中没有变量，因此指令后的操作数一般是寄存器。

RISC-V中有32个寄存器（x0-x31），每个都是32位宽
* x0恒等于0，因此实际上有31个可用寄存器

# add指令和sub指令

## add

指令格式：add x1, x2, x3
对应：$a = b + c$

## sub

指令格式：sub x1, x2, x3
对应：$a = b - c$

## 进行更复杂的运算

进行更复杂的运算，需要使用临时变量，例如对于$a = b + c + d - e$:
* add x10, x1, x2  # $atemp = b + c$
* add x10, x10, x3  # $atemp = atemp + d$
* sub x10, x10, x4  # $a = atemp - e$

# Immediate

指令格式：addi x1, x2, 10
对应：$a = b + 10$
    
不需要subi，因为addi中的立即数可以是负数