CXX = g++
CXXFLAGS = -O2 -g -std=c++14 -Wall
LIBS = -lm

.PRECIOUS = %.o

APPS = find_if.exe permutations.exe generate.exe for_each.exe \
       particle_sort.exe count_clamp.exe find_words.exe zip_it.exe \
       accumulate.exe

all: $(APPS)

%.exe: %.o
	$(CXX) $(CXXFLAGS) -o $@ $^ $(LIBS)

%.o: %.cpp
	$(CXX) $(CXXFLAGS) -c -o $@ $<

.PRECIOUS: %.o

clean:
	rm -f $(APPS) *.o *.gch
