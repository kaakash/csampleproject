# Makefile compiles all C files preset in a folder 
# Generates teh .o files in the obj folder and creates
# binary in /bin folder 

# initializing constants 
CC=gcc
CFLAGS=-c

# finding all c files in the folder and replacing their extensions with 
# .o to get all the object files 
# NOTE : we can also directly look for .o files in the obj directory using 
# teh wildcard function if we dont have a one to one mapping

OBJECTS=$(patsubst %.c, ../obj/%.o, $(wildcard *.c))

# rule for compiling to a binary 
all: ../bin/hello

../obj/%.o: %.c
	$(CC) $(CFLAGS) $< -o $@

../bin/hello: $(OBJECTS)
	$(CC) $< -o $@

# rule for cleaning the compiled output
clean:
	rm ../obj/*o ../bin/hello
