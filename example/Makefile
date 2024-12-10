include ../makefiles/embedded.defs

all: build/mandelbrot.hex

build/mandelbrot.hex: build mandelbrot.c
	$(COMPILE) -O5 -DF_CPU=50000000 -DCPU_PIPELINED -T$(LIBDIR)/map_ecp5.ld mandelbrot.c -o build/mandelbrot.elf
	$(OBJCOPY) build/mandelbrot.elf --hex -o build/mandelbrot.hex

build:
	mkdir -p build

.PHONY: clean
clean:
	rm -rf ./build