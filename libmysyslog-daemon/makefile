CC = gcc
CFLAGS = -Wall -g -I/home/a2da/mysyslog/libmysyslog -I/home/a2da/mysyslog/libmysyslog-text -I/home/a2da/mysyslog/libmysyslog-json
LDFLAGS = -L/home/a2da/mysyslog/libmysyslog -L/home/a2da/mysyslog/libmysyslog-text -L/home/a2da/mysyslog/libmysyslog-json -lmysyslog -lmysyslog-text -lmysyslog-json
all: libmysyslog-daemon

libmysyslog-daemon: libmysyslog-daemon.o
	$(CC) -o $@ $^ $(LDFLAGS)

libmysyslog-daemon.o: libmysyslog-daemon.c
	$(CC) $(CFLAGS) -c $<

run: libmysyslog-daemon
	./libmysyslog-daemon

clean:
	rm -f libmysyslog-daemon *.o
