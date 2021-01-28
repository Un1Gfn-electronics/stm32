STM32F103C8T6
STM32-F103-C8-T6

https://en.wikipedia.org/wiki/STM32#STM32_F1
ARM Cortex-M3 Instruction Set

https://www.st.com/en/microcontrollers-microprocessors/stm32f103.html
STM32F103C8 - datasheet
https://www.st.com/content/st_com/en/products/microcontrollers-microprocessors/stm32-32-bit-arm-cortex-mcus/stm32-mainstream-mcus/stm32f1-series/stm32f103/stm32f103c8.html

USB 2.0 full-speed interface

Built-in
Crystal oscillator
Flash memory
SRAM
SysTick timer

https://www.st.com/content/st_com/en/products/microcontrollers-microprocessors/stm32-32-bit-arm-cortex-mcus/stm32-mainstream-mcus/stm32f1-series/stm32f103/stm32f103c8.html#resource
AN2586 - Getting started with STM32F10xxx hardware development
         reference hardware design w/ SWJ (Serial wire JTAG)
DS5319 - Datasheet
         power supply scheme, 
PM0056 - Instruction set
AN2606 - STM32 microcontroller system memory boot mode
AN4879 - USB hardware and PCB guidelines using STM32 MCUs
RM0008 - Reference manual

HW Model, CAD Libraries & SVD?
Presentations & Training Material?



https://www.st.com/resource/en/datasheet/stm32f103c8.pdf
https://www.alldatasheet.com/view.jsp?Searchword=Stm32f103c8t6

https://blog.podkalicki.com/how-to-compile-and-burn-the-code-to-stm32-chip-on-linux-ubuntu/
https://startingelectronics.org/tutorials/STM32-microcontrollers/programming-STM32-flash-in-Linux/
https://stackoverflow.com/questions/37644823/how-to-flash-stm32-using-only-linux-terminal

9 communication interfaces
2 I2C SMBus PMBus
3 USART ISO 7816
2 SPI
1 CAN
1 USB 2.0

Software
Fully compatible w/ STM32F103
https://github.com/texane/stlink/
https://github.com/texane/stlink/blob/master/doc/tested-boards.md
https://sourceforge.net/projects/stm32flash/
https://aur.archlinux.org/packages/arm-none-eabi-gcc74-linaro/

Build a prototype programmer
http://www.micromouseonline.com/2014/01/05/mini-st-linkv2-programmer/
USB_DM USBDM USB_DP USBDP
https://www.st.com/resource/en/datasheet/stm32f103c8.pdf#page=31
https://www.st.com/resource/en/datasheet/stm32f103c8.pdf#page=74
M3480I?
https://www.alldatasheet.com/view.jsp?Searchword=M3480I
Extract info about connection from discovery board pcb file



Bus 003 Device 005: ID 10c4:ea60 Silicon Labs CP210x UART Bridge


=============================================================================


Bus 003 Device 006: ID 0483:3748 STMicroelectronics ST-LINK/V2


page 22 - LQFP100 pins

https://www.st.com/content/st_com/en/products/development-tools/hardware-development-tools/hardware-development-tools-for-stm32/st-link-v2.html#resource




arm-none-eabi-gcc


arm-none-eabi-gcc -std=gnu99 -g -O2 -Wall -mlittle-endian -mthumb -mthumb-interwork -mcpu=cortex-m0 -fsingle-precision-constant -Wdouble-promotion loop.c -o main.elf

arm-none-eabi-gcc -std=gnu99 -g -O2 -Wall -mlittle-endian -mthumb -mthumb-interwork -mcpu=cortex-m3 -fsingle-precision-constant -Wdouble-promotion loop.c -o main.elf



export
  LD_LIBRARY_PATH="$LD_LIBRARY_PATH:$HOME/stlink/build/Release/_install/usr/local/lib"

https://stackoverflow.com/questions/2548486/compiling-without-libc

arm-none-eabi-gcc -Wall -Wextra -mlittle-endian -nostdlib -mcpu=cortex-m3 main.c -o main.elf


arm-none-eabi-objcopy -O binary main.elf main.bin

https://blog.podkalicki.com/how-to-compile-and-burn-the-code-to-stm32-chip-on-linux-ubuntu/

st-link v2
https://www.st.com/content/st_com/en/products/development-tools/hardware-development-tools/hardware-development-tools-for-stm32/st-link-v2.html
