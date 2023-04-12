# Macros                                                                        
CC=gcc217

# Dependency rules for non-file targets                                         
all: ft
clobber: clean
        rm -f ft_client.o *~
clean:
        rm -f ft

# Dependency fules for file targets                                             
ft: ft.o ft_client.o
        $(CC) ft.o ft_client.o -o ft

ft_client.o: ft_client.c ft.h a4def.h
        $(CC) -c ft_client.c

ft.o: ft.c dynarray.h path.h ft.h checkerDT.h dNode.h
        $(CC) -c ft.c

