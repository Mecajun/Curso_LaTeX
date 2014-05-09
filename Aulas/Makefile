##
# Makefile for Latex
# @author Rafael Lima
# @version 1.33
##

# Compiler Options
CC = pdflatex
CCFLAGS = --enable-write18

NAME = cursolatex

##
# Recipes:
##
.PHONY = ALL
ALL: $(NAME).pdf

# Compile and open pdf
$(NAME).pdf: $(NAME).tex
	$(CC) $(CCFLAGS) $< &&	$(CC) $< && $(CC) $< &&\
	mv $(@) ../$(@)&&\
	xdg-open ../$(@)&

# Remove generated files
.PHONY = clean
clean:
	rm -f *.aux $(NAME).bbl $(NAME).blg $(NAME).log $(NAME).idx $(NAME).out \
	$(NAME).nav $(NAME).snm $(NAME).toc $(NAME).vrb $(NAME).nav

.PHONY = clean-all
clean-all: clean
	rm -f ../$(NAME).pdf