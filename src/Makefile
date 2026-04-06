PROGRAM = chapter_exe
OBJS = chapter_exe.o mvec.o

CC = gcc
CFLAGS = -O3 -I/usr/local/include/avisynth -ffast-math -Wall -Wshadow -Wempty-body -I. -std=gnu++11 -fpermissive -fomit-frame-pointer -s -fno-tree-vectorize -DSYS_MACOSX -DSYS_ARM64 -DSYS_MACOSX -DSYS_ARM64 
LDLAGS = -ldl -lstdc++ -pthread

.SUFFIXES: .c .o

$(PROGRAM): $(OBJS)
	$(CC) -o $(PROGRAM) $^ $(LDLAGS)

.cpp.o:
	$(CC) $(CFLAGS) -c $<

.PHONY: clean
clean:
	$(RM) $(PROGRAM) $(OBJS)
