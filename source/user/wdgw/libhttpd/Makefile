TARGET = libhttpd.a
CFLAGS += -I../

OBJS = protocol.o api.o version.o ip_acl.o

all: $(OBJS)
	$(AR) cr $(TARGET) $(OBJS)

romfs:


clean:
	rm -f $(TARGET) *.o
