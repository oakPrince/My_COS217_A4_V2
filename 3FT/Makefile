GCC = gcc217
all: ft

clobber: clean
	rm -f dynarray.o path.o checkerDT.o ft.o ft_client.o dNode.o *~

clean:
	rm -f $(ft) meminfo*.out

dynarray.o: dynarray.c dynarray.h
	gcc217 -c dynarray.c 

path.o: path.c dynarray.h path.h a4def.h
	$(GCC) -g -c $<

dNode.o: dNode.c dynarray.h checkerDT.h dNode.h path.h a4def.h
	$(GCC) -g -c $<

checkerDT.o: checkerDT.c dynarray.h checkerDT.h dNode.h path.h a4def.h
	$(GCC) -g -c $<

ft: ft_client.o ft.o dynarray.o dNode.o path.o checkerDT.o
	gcc217 ft_client.o ft.o dynarray.o dNode.o path.o checkerDT.o -o ft

ft_client.o: ft_client.c ft.h
	gcc217 -c ft_client.c 

ft.o: ft.c ft.h a4def.h dynarray.h path.h checkerDT.h dNode.h
	gcc217 -c ft.c
