
OBJECTS = FileRead.o 		\
	  	  FrameExtractor.o 	\
		  H263Frames.o		\
		  H264Frames.o		\
		  MPEG4Frames.o		\
		  VC1Frames.o

SRCS = $(OBJECTS:.o=.c)
DEPENDENCY = FileRead.h 		\
		     FrameExtractor.h 	\
		     H263Frames.h 		\
		     H264Frames.h 		\
		     MPEG4Frames.h 		\
		     VC1Frames.h 		

AR = arm-linux-ar
AFLAGS = crv
CC = arm-linux-gcc
CFLAGS = -c -Wall -g -Os -std=gnu99 

INC = -I../Common

TARGET = libFrameExtractor.a

$(TARGET) : $(OBJECTS)
	$(AR) $(ARFLAGS) $@ $(OBJECTS)

.c.o :
	$(CC) $(INC) $(CFLAGS) $<

clean :
	rm -rf $(OBJECTS) $(TARGET)

FileRead.o : $(DEPENDENCY) FileRead.c
FrameExtractor.o : $(DEPENDENCY) FrameExtractor.c
H263Frames.o : $(DEPENDENCY) H263Frames.c
H264Frames.o : $(DEPENDENCY) H264Frames.c
MPEG4Frames.o : $(DEPENDENCY) MPEG4Frames.c
VC1Frames.o : $(DEPENDENCY) VC1Frames.c

