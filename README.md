# OS
to create a simple operator system for learn basic computer knowledge.

工具：
 1. windows平台使用WSL作为子系统
 2. NASM作为编译器
 3. QEMU作为运行环境

<!-- 2026.03.28 -->
1. 电脑上电，从主板的FLASH上加载BIOS，这个是固件代码，由硬件厂家提供
2. BIOS加载外部存储介质的第一个扇区512Byte,将代码加载到内存的0x7c00处执行，
   这512Byte就是bootloader
3. boot代码需要满足两个条件： 512字节大小；最后两个字节分别为0xaa55;
boot1.asm代码分析：
    
