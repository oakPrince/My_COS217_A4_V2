# Macros                                                                        
CC=gcc217

# Dependency rules for non-file targets                                         
all: ft
clobber: clean
        rm -f ft_client.o checkerDT.o dNode.o dynarray.o path.o *~
clean:
        rm -f ft

# Dependency fules for file targets                                             
ft: ft.o ft_client.o checkerDT.o dNode.o dynarray.o path.o
        $(CC) ft.o ft_client.o checkerDT.o dNode.o dynarray.o path.o -o ft

ft_client.o: ft_client.c ft.h a4def.h
        $(CC) -c ft_client.c

ft.o: ft.c ft.h dynarray.h checkerDT.h dNode.h path.h
        $(CC) -c ft.c

dynarray.o: dynarray.c dynarray.h
        $(CC) -c dynarray.c
        
path.o: path.c dynarray.h path.h a4def.h
        $(CC) -c path.c

dNode.o: dNode.c dynarray.h checkerDT.h dNode.h path.h a4def.h
        $(CC) -c dNode.c
        
checkerDT.o: checkerDT.c dynarray.h checkerDT.h dNode.h path.h a4def.h
        $(CC) -c checkerDT.c
