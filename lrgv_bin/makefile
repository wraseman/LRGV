MAIN_DIR=./..
SOURCE_DIR = $(MAIN_DIR)/lrgv_src
SOURCES =                       \
    $(SOURCE_DIR)/moeaframework.c             \
    $(SOURCE_DIR)/lrgv_functions.cpp             \
    $(SOURCE_DIR)/lrgv_input.cpp             \
    $(SOURCE_DIR)/lrgv_main.cpp             \
    $(SOURCE_DIR)/lrgv_memory.cpp             \
    $(SOURCE_DIR)/lrgv_rand.cpp             \
    $(SOURCE_DIR)/lrgv_roulette.cpp             \
	$(SOURCE_DIR)/lrgv_Simulation.cpp	\
    $(SOURCE_DIR)/lrgv_utility.cpp             \
	$(SOURCE_DIR)/rand.cpp \

OBJECTS=$(SOURCES:.cpp=.o)
CC=g++
#CC=icpc
CFLAGS=-c -O3 -Wall -I. -I$(SOURCE_DIR) -DLINUX
#CFLAGS=-c -g -O3 -Wall -I. -I$(SOURCE_DIR) -DLINUX
#LDFLAGS=-g -L./lib 
EXECUTABLE=lrgv

all: $(SOURCES) $(EXECUTABLE)
	rm -rf $(SOURCE_DIR)/*.o

$(EXECUTABLE): $(OBJECTS)
	$(CC) $(OBJECTS) $(LDFLAGS) -o $@

.cpp.o:
	$(CC) $(CFLAGS) $^ -o $@

clean:
	rm -rf $(SOURCE_DIR)/*.o $(EXECUTABLE)
