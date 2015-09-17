# This makefile will just call the makefile from the src directory and 
# will create a delivery package if required. 

.PHONY: all
all:
	cd src && make

.PHONY: clean
clean:
	rm ./obj/*o ./bin/hello ./*tar.gz

.PHONY: package
package:
	tar -zcvf software.tar.gz ./lib ./bin ./doc ./man
