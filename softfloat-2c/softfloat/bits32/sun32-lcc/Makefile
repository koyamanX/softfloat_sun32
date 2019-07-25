
PROCESSOR_H = ../../../processors/sun32-lcc.h
SOFTFLOAT_MACROS = ../softfloat-macros

OBJ = .o
EXE = softfloat
INCLUDES = -I. -I..
COMPILE_C = sun32-unknown-elf-lcc -c -o $@ $(INCLUDES) -I -O2
LINK = sun32-unknown-elf-ld -o $@

#------------------------------------------------------------------------------
# Probably okay below here.
#------------------------------------------------------------------------------

ALL: softfloat$(OBJ) 

milieu.h: $(PROCESSOR_H)
	touch milieu.h

softfloat$(OBJ): milieu.h softfloat.h softfloat-specialize $(SOFTFLOAT_MACROS) ../softfloat.c
	$(COMPILE_C) ../softfloat.c


