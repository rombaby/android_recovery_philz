# path to toolchain
PATH := /home/changyuet/cm11/prebuilt/linux-x86/toolchain/arm-eabi-4.4.3/bin:$(PATH)

# NDK
CC := arm-linux-androideabi-gcc
STRIP := arm-linux-androideabi-strip

# gcc
# CC := gcc
# STRIP := strip

WFLAGS += -Wall -Wextra -Wno-write-strings
CFLAGS += $(WFLAGS) -g -static -DANDROID
LDFLAGS += -lpng -lz -lm
OBJECTS += fb2png adb_screenshoot

ALL: $(OBJECTS)

fb2png: main.o fb2png_main.o fb.o img_process.o fb2png.o
	$(CC) $(CFLAGS) main.o fb2png_main.o fb.o img_process.o fb2png.o -o fb2png $(LDFLAGS)

adb_screenshoot: adb_screenshoot.o fb.o img_process.o
	$(CC) $(CFLAGS) adb_screenshoot.o fb.o img_process.o -o adb_screenshoot $(LDFLAGS)

strip:
	$(STRIP) --strip-unneeded $(OBJECTS)
	$(STRIP) --strip-debug $(OBJECTS)

clean:
	rm -f *.o
	rm -f fb2png adb_screenshoot
