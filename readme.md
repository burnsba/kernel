Build with:

    nasm -f elf32 kernel.asm -o kasm.o

    gcc -m32 -c kernel.c -o kc.o

    ld -m elf_i386 -T link.ld -o kernel kasm.o kc.o
	
For grub2, copy kernel to /boot/ and just run 'update-grub'

- reboot
- press 'c' from advanced grub menu to open limited shell
- grub> multiboot /boot/kernel-1
- (nothing happens)
- hit escape
- Select kernel to boot; displays same error
- press any key
- kernel loads

http://download-mirror.savannah.gnu.org/releases/grub/phcoder/multiboot.pdf  
http://forum.osdev.org/viewtopic.php?f=1&t=16757   
http://wiki.osdev.org/Creating_a_64-bit_kernel   