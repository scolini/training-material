ICC = icc
ICFLAGS = -qopenmp -O2 -g -Wall -Wremarks -Wcheck -w3 -diag-enable openmp -w2547

GCC = gcc
GCFLAGS = -fopenmp -O2 -g -Wall -W

all: false_sharing_correct_icc.exe false_sharing_correct_gcc.exe \
     false_sharing_intel_problem_icc.exe false_sharing_intel_problem_gcc.exe

%_icc.exe: %.c
	$(ICC) $(ICFLAGS) -o $@ $<

%_gcc.exe: %.c
	$(GCC) $(GCFLAGS) -o $@ $<

clean:
	rm -f *.exe *.o
