# make with make -f roughness_metrics_driver.make

CC=g++
CFLAGS=-c -Wall -O3  -g
OFLAGS = -Wall -O3
LDFLAGS= -Wall
SOURCES=roughness_metrics_driver.cpp ../LSDIndexRaster.cpp ../LSDRaster.cpp ../LSDStatsTools.cpp ../LSDShapeTools.cpp
LIBS= -lm -lstdc++ 
# -lfftw3
OBJECTS=$(SOURCES:.cpp=.o)
EXECUTABLE=roughness_metrics_driver

all: $(SOURCES) $(EXECUTABLE)

$(EXECUTABLE): $(OBJECTS)
	$(CC) $(OFLAGS) $(OBJECTS) $(LIBS) -o $@
	cp $(EXECUTABLE) ../data/

.cpp.o:
	$(CC) $(CFLAGS) $< -o $@

clean:
	rm -rf *.o 
	rm -rf ../*.o 
