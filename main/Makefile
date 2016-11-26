include ../config.mk
include ../server.mk

EXTRALIB += -lmp4v2 -lpthread -lm 

OBJS = mp4to264.o
TARGET = mp4to264

all : $(TARGET)
$(TARGET) : $(OBJS)
	/bin/rm -f -f $(TARGET)
	$(CC) $(CFLAGS) -o $@ $(OBJS) $(LDFLAGS) $(EXTRALIB)	
ifeq ($(RELEASE),y)	
	$(STRIP) $(TARGET)
endif	

.PHONY: clean

clean: 
	/bin/rm -f -f $(TARGET)
	/bin/rm -f -f *.o
    