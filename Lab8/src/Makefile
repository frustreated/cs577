# Bradford Smith (bsmith8)
# Makefile for CS 577 Lab 8
# 11/19/2015
# "I pledge my honor that I have abided by the Stevens Honor System."
################################################################################

PRG=sniffer
AUTHOR=bsmith8
PROJECT=cs577-lab8
SRC=main.c filterEthernet.c hexify.c count.c search.c flows.c node.c
OBJ=$(SRC:.c=.o)
CC=gcc
RM=rm -f
INCLPATH=-I../include
LIBPATH=
LDLIBS=-lpcap
LDFLAGS+=
# implicit compiling rules:
# C complied with: `$(CC) -c $(CPPFLAGS) $(CFLAGS)`
CFLAGS+= $(INCLPATH)
CPPFLAGS+= -pedantic-errors -Wall
DBFLGS= -g -DDEBUG

all: $(OBJ)
	$(CC) $(LDFLAGS) $(OBJ) $(LDLIBS) -o $(PRG)

debug: fclean
debug: CPPFLAGS+= $(DBFLGS)
debug: all

clean:
	$(RM) *.o

fclean: clean
	$(RM) $(PRG)

re: fclean all

tar: fclean
	tar -cvzf ../../$(AUTHOR)_$(PROJECT).tar.gz ../*

