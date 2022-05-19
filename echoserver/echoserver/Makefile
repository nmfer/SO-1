CC = gcc

#Release Flags
CFLAGS = -O2 -Wall -I .

#DebugFlags
#CFLAGS = -g -Wall -I .

# This flag includes the Pthreads library on a Linux box.
# Others systems will probably require something different.
LIB = -lpthread

all: mainserver mainclient

mainserver: mainserver.c csapp.o
	$(CC) $(CFLAGS) -o mainserver mainserver.c csapp.o $(LIB)

csapp.o:
	$(CC) $(CFLAGS) -c csapp.c

mainclient: mainclient.c
	$(CC) $(CFLAGS) -o mainclient mainclient.c csapp.o $(LIB)
	

clean:
	rm -f *.o mainserver mainclient*~
	(cd cgi-bin; make clean)
	(cd libtomcrypt ; make clean)
