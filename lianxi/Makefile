CC = gcc
CFLAGS = -c -Wall 
TOPDIR = $(PWD)
OBJDIR = $(TOPDIR)/obj/
SRCDIR = $(TOPDIR)/src/
INCDIR = $(TOPDIR)/inc/
BINDIR = $(TOPDIR)/bin/
SRCLIST = $(wildcard $(SRCDIR)*.c)
OBJTEMO = $(basename $(SRCLIST))
OBJTEMP1 = $(addsuffix .o ,$(OBJLIST))
#OBJTEMP2 = $(notdir $(OBJTEMP))
OBJ = $(addprefix $(OBJDIR),$(OBJTEMP1))
BIN = $(BINDIR)test

all:CHECKDIR test
CHECKDIR:
	mkdir -p $(OBJDIR) $(BINDIR)
test:$(BIN)
$(BIN):$(OBJ)
	$(CC) $^ -o $@
$(OBJDIR)%.o:$(SRCDIR)%.c
	$(CC) $(CFLAGS) $^ -o $@
.PHONY:clean
clean:
	rm -rf $(OBJDIR) $(BINDIR)
