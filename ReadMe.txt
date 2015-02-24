========================================================================
    CONSOLE APPLICATION : Lexical Analyzer Project Overview
========================================================================

lex.cpp
    This is the main application source file. The analyzer is for C source code. Some operators are missing such as -> and ++ and other 
	2-character operators. The program will ask the user to input a file name to be lexically analyzed. Then the program will tokenize all of
	the input file based on delimiters (whitespace, commas, symbols, and operators). 
	These tokens are then analyzed further to determine the type (keyword, identifier, integer, float, operator, symbol). The program then prints
	out the token and the type of that token.

DFA.h and DFA.cpp
	These files define a class that makes a similar DFA from lab1. The DFA class is used in lex.cpp to test if tokens are a part of a given langauge. 
	It is essentially a regular expression checker. This is used to see if a given string is a valid C identifier, integer, float, or string literal.
	The DFA class takes an input file upon construction, in which it loads in the rules for the language (the same way it did in lab1).

/////////////////////////////////////////////////////////////////////////////
Other standard files:

StdAfx.h, StdAfx.cpp
    These files are used to build a precompiled header (PCH) file
    named Lexical Analyzer.pch and a precompiled types file named StdAfx.obj.

test1.txt, test2.txt and test3.txt are input files used to test lex.cpp. They contain simple C source code.
test2.txt containes 1 error for the sake of testing incorrect identifiers. The other 2 test files contain valid C code.
identifier.txt, integer.txt, float.txt, and string.txt are used by DFA.cpp to initialize the regular language that the DFA checks. 
keywords and symbols are done without the need to make a DFA because they can be easily checked with some if statements inside lex.cpp