CC=nvcc
CCFLAGS=-ccbin g++ -m64 -gencode arch=compute_50,code=sm_50 -Wno-deprecated-gpu-targets
FILE=hello
RM=rm -f

$(FILE).out: $(FILE).cu
	$(CC) $(CCFLAGS) $^ -o $@

all: $(FILE).out
	./$(FILE).out

clean:
	$(RM) $(FILE).out
