CFLAGS=-D_LINUX -fPIC -Iinclude -Ivc++
OBJS=liba52/bit_allocate.o liba52/bitstream.o liba52/downmix.o liba52/imdct.o liba52/parse.o

ac3codec-i486-linux.so: $(OBJS)
	gcc -fPIC -shared -o $@ $(OBJS) `cat ../../../XBMC/xbmc/cores/DllLoader/exports/wrapper.def` ../../../XBMC/xbmc/cores/DllLoader/exports/wrapper.o

clean:
	$(RM) $(OBJS) *.so

%o : %c
	gcc $(CFLAGS) -O2 -fPIC -c $< -o $@

%o : %cpp
	g++ $(CFLAGS) -O2 -fPIC -c $< -o $@
