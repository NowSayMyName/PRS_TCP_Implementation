all: mainServer mainClient

mainTest: test.o
	gcc -Wall test.o -o mainTest

test.o: test.c
	gcc -Wall test.c -I./include -c -o test.o
	
mainServer: server.o connection.o
	gcc -Wall server.o connection.o -o mainServer

server.o: server.c
	gcc -Wall server.c -I./include -c -o server.o

mainClient: client.o connection.o
	gcc -Wall client.o connection.o -o mainClient

client.o: client.c
	gcc -Wall client.c -I./include -c -o client.o

connection.o: connection.c
	gcc -Wall connection.c -I./include -c -o connection.o

clean:
	rm -f *.o