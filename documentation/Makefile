UNAME=$(shell uname)

CCFLAGS=-Wall -Wextra -Wno-unused-parameter -O3
ifdef CTEST_COLOR_OK
CCFLAGS+=-DCOLOR_OK
endif

ifeq ($(UNAME), Darwin)
LDFLAGS=-Wl,-flat_namespace,-undefined,dynamic_lookup
endif

all: test

remake: clean all

%.o: %.c ctest.h
	gcc $(CCFLAGS) -c -o $@ $<

example0: example0.o
	gcc $(LDFLAGS) example0.o -o test

clean:
	rm -f test *.o

