# Define the compiler
CXX = g++

# Define the compiler flags
CXXFLAGS = -Wall -Wextra -std=c++11

# Define the sources and headers
SRCS = main.cpp glad.c
HEADERS = glad.h

# Define the object files
OBJS = main.o glad.o

# Define the executable name
TARGET = GLFW_test.exe

LIBS = -lglfw -lGLEW -lGL

# Default target to build the project
all: $(TARGET)

# Rule to link the object files to create the executable
$(TARGET): $(OBJS)
	$(CXX) $(CXXFLAGS) -o $(TARGET) $(OBJS) $(LIBS)

# Rule to compile the source files into object files
main.o: main.cpp
	$(CXX) $(CXXFLAGS) -c main.cpp -o main.o

glad.o: glad.c
	$(CXX) $(CXXFLAGS) -c glad.c -o glad.o

# Clean rule to remove object files and the executable
clean:
	rm -f $(OBJS) $(TARGET)

# Phony targets
.PHONY: all clean
