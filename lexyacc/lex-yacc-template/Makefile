LC=lex.yy.c
YC=y.tab.c
all: count-lines count-lwc count-num calc text-cleanup

optional: ex1 ex2 ex3 ex4

calc: calc.l calc.y
	yacc -d $@.y
	lex $@.l
	gcc -o $@ $(LC) $(YC)

%: %.l
	lex $^
	gcc -o $@ $(LC) -ll
