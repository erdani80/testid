CC = gcc
CFLAGS  = -g -Wall
LIBS = -lm

default: id_server id_client

id_server:  id_server.o cJSON.o
	$(CC) $(CFLAGS) $(LIBS) -o id_server id_server.o cJSON.o

id_client:  id_client.o cJSON.o 
	$(CC) $(CFLAGS) $(LIBS) -o id_client id_client.o cJSON.o

id_server.o:  id_server.c 
	$(CC) $(CFLAGS) -c id_server.c

id_client.o:  id_client.c                       
	$(CC) $(CFLAGS) -c id_client.c

cJSON.o:  cJSON.c cJSON.h 
	$(CC) $(CFLAGS) -c cJSON.c

clean: 
	$(RM) id_server id_client *.o *~

