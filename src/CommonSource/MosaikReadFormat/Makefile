# ==================================
# MOSAIK Mosaik Read Format Makefile
# (c) 2008 Michael Stromberg
# ==================================

# -------------------
# define our includes
# -------------------
TD = ../../
INCLUDES = -I$(TD)$(DATA_STRUCT_DIR) -I$(TD)$(CONFIG_DIR) -I$(TD)$(UTILITIES_DIR) -I.

# ----------------------------------
# define our source and object files
# ----------------------------------
SOURCES= AlignmentReader.cpp AlignmentWriter.cpp ReadReader.cpp ReadWriter.cpp ReferenceSequenceReader.cpp
OBJECTS= $(SOURCES:.cpp=.o)
BUILT_OBJECTS= $(patsubst %,$(TD)$(OBJ_DIR)/%,$(OBJECTS))

all: $(BUILT_OBJECTS)

.PHONY: all

$(BUILT_OBJECTS): $(SOURCES)
	@echo "  * compiling" $(*F).cpp
	@$(CXX) -c -o $@ $(*F).cpp $(CXXFLAGS) $(PLATFORM_FLAGS) $(INCLUDES)

clean:
	@echo "Cleaning up."
	@rm -f $(TD)$(OBJ_DIR)/* $(TD)$(BIN_DIR)/*

.PHONY: clean
