#
# Makefile for utility tools.
#
# Author: Michael Morckos <mmorckos@uwaterloo.ca>
#

##### Source directory #####
SRC_DIR		= .
SUBDIRS		= third_party

##### Compiler, tools and options #####
CXX		= @echo compiling $< && g++

##### Prerequisites #####
$(EVERYTHING)::
	@for subdir in $(SUBDIRS); \
	do \
	    echo "making $@ in $$subdir"; \
	    ( cd $$subdir && $(MAKE) $@ ) || exit 1; \
	done

##### Targets #####
all:	xmlglobalserviceparser.o	dataformatconverter.o

xmlglobalserviceparser.o:	$(SRC_DIR)/xmlglobalserviceparser.cpp
	$(CXX) -c $(SRC_DIR)/xmlglobalserviceparser.cpp
	
#xmlserviceparser.o:	$(SRC_DIR)/xmlserviceparser.cpp
#	$(CXX) -c $(SRC_DIR)/xmlserviceparser.cpp
	
#configparser.o:	$(SRC_DIR)/configparser.cpp
#	$(CXX) -c $(SRC_DIR)/configparser.cpp

#serviceparser.o:	$(SRC_DIR)/serviceparser.cpp
#	$(CXX) -c $(SRC_DIR)/serviceparser.cpp
	
dataformatconverter.o:	$(SRC_DIR)/dataformatconverter.cpp
	$(CXX) -c $(SRC_DIR)/dataformatconverter.cpp

clean:
	rm -f *.o
	
install:: all
