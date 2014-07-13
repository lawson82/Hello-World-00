SUBDIRS = cJSON libhttpd src

all:
	for i in $(SUBDIRS) ; do $(MAKE) -C $$i $@ || exit $?; done

romfs:
	for i in $(SUBDIRS) ; do $(MAKE) -C $$i $@ || exit $?; done

clean:
	for i in $(SUBDIRS) ; do $(MAKE) -C $$i $@ || exit $?; done
