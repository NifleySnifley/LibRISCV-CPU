include ../makefiles/bootloader.defs

all: build/bootloader_v2.hex

build/bootloader_v2.hex: build bootloader_v2.c
	$(COMPILE_FULL) -nostdlib -Os bootloader_v2.c -o build/bootloader_v2.elf
	riscv32-unknown-elf-size build/bootloader_v2.elf
	$(OBJCOPY) build/bootloader_v2.elf --hex -o build/bootloader_v2.hex

build:
	mkdir -p build

.PHONY: clean
clean:
	rm -rf ./build