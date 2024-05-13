# intro

* 电线 -> 二进制编码

![format](image-8.png)

# R-Format

* 用于逻辑或算数的寄存器到寄存器的指令
* 格式：
![R](image-9.png)
    * R-format的opcode都为0110011（6位到0位）
    * funct7+funct3决定运行哪种指令（例如add）

![all R](image-10.png)

# I-Format

* 与寄存器和立即数有关的指令和load
![I](image-11.png)

![all I](image-12.png)

## Load

* 与I类指令格式相同，opcode不同
![Load](image-13.png)

# S-format

* 只有store指令
![S](image-14.png)
![S](image-15.png)

