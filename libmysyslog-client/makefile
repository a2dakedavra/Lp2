CC = gcc
CFLAGS = -Wall -g -I/home/a2da/mysyslog/libmysyslog -I/home/a2da/mysyslog/libmysyslog-text -I/home/a2da/mysyslog/libmysyslog-json
LDFLAGS = -L/home/a2da/mysyslog/libmysyslog -L/home/a2da/mysyslog/libmysyslog-text -L/home/a2da/mysyslog/libmysyslog-json -lmysyslog -lmysyslog-text -lmysyslog-json

all: libmysyslog-client

libmysyslog-client: libmysyslog-client.o
	$(CC) -o $@ $^ $(LDFLAGS)

libmysyslog-client.o: libmysyslog-client.c
	$(CC) $(CFLAGS) -c $<

run: libmysyslog-client
	./libmysyslog-client

clean:
	rm -f libmysyslog-client *.o
