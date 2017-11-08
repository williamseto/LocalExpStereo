all: LocalExpStereo

#set these to the location of your header files
OPENCV_INC_DIR=/usr/local/Cellar/opencv/3.3.0_3/include/opencv2/core/
OMP_INC_DIR = /usr/local/opt/llvm/include/
OMP_LIB_DIR = /usr/local/opt/llvm/lib/
CXXFLAGS = $(shell pkg-config --libs --cflags opencv)
CXXFLAGS += -w -fopenmp -std=c++14 -stdlib=libc++
CC = /usr/local/opt/llvm/bin/clang++

LocalExpStereo: *.cpp *.h Makefile
	$(CC) $(CXXFLAGS) -o LocalExpStereo *.cpp ../maxflow/*.cpp -I$(OPENCV_INC_DIR) -I$(OMP_INC_DIR) -L$(OMP_LIB_DIR)
