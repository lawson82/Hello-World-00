WDGW_OBJS = commandline.o \
	conf.o \
	debug.o \
	fw_iptables.o \
	firewall.o \
	gateway.o \
	centralserver.o \
	http.o \
	auth.o \
	client_list.o \
	util.o \
	wdctl_thread.o \
	ping_thread.o \
	safe.o \
	httpd_thread.o \
	../libhttpd/libhttpd.a \
	../cJSON/libjson.a

WDCTL_OBJS = wdctl.o

CFLAGS += -I../libhttpd/ -I../cJSON/
LDLIBS += -lpthread

all: wdgw wdctl
wdgw: $(WDGW_OBJS)
	$(CC) -o wdgw $(WDGW_OBJS) $(LDLIBS)

wdctl: $(WDCTL_OBJS)
	$(CC) -o wdctl $(WDCTL_OBJS) $(LDLIBS)

romfs:
	$(ROMFSINST) wdgw /bin/wdgw
	$(ROMFSINST) wdctl /bin/wdctl

clean:
	rm -f *.o wdgw wdctl
