SIMPLE SHELL

SYNOPSIS

FILE & FUNCTION DESCRIPTIONS

Files	Descriptions
built_in.c	handles and contains built in shell functions
error_elephant.c	file containing error processing and writing directives
freedom.c	various functions associated with preventing memory leaks
man_1_simple_shell	Manual page
help_fun.c	misc. functions that serve aux purposes
main.c	entry point for simple shell program
pathfinder.c	has functions associated with tokenizing PATH and checking pathArr against command
shell.h	header file for the simple shell program that includes protos librars and structs
string_support.c	this file consists of string manipulation functions called in various support roles
tokenizer.c	contains tokstr as well as its associated support subfunctions
Functions	Descriptions
built_in.c	
int runBuiltIn(char **command, char *line)	check for then calls built in functions
int hey_exit(char **command)	executes built in shell exit
int hey_env(char **command)	prints user's current env to SO
error_elephant.c	
void errorHand(int lNum, char *arg, char *pName)	writes error msgs to stderr
freedom.c	
void free_tokens(char **tokens)	frees command array and its components
void free_path(char **paths)	frees path array and its components
void free_env(void)	frees environment (used for testing)
void free_exit(char *line)	prepares for program exit
void sig_stop(int sNum)	traps SIGINT and taunts user
help_fun.c	
char **get_input(char *input)	supplies tokstr with delims for command
char *_itoa(int num)	converts int to str for err msgs
int forktime(char **command, char *thePath)	forks process and executes commands
int cleanstr(char *line)	removes new lines from line str
int num_len(int num)	counts digits in num for err msgs
pathfinder.c	
char **path_locate(char *envvar)	find PATH env var and supplies to tokstr
char **path_tok(char *path)	supplies delims for path tokenization
char *check_paths(char *command)	checks and cats command and pathArr
string_support.c	
char *_strcat(char *dest, char *src)	concats src str onto dest str
char *_strcpy(char *dest, char *src)	copies src str into dest str
int _strlen(char *s)	calc length of str
int _strncmp(char *s1, char *s2, int n)	compares first n bytes of two strs
int _strcmp(char *s1, char *s2)	finds first dif char in two strs
tokenizer.c	
int tok_num(char *str, char *delims)	computes num of toks in str w/ delims
int substrLen(char *str, char *delims)	calculates length of substring
char **tokstr(char *line, char *delims)	tokenizes str into arr of substrs


BUILT-INS
exit
exits shell (Usage: exit [status])

env
prints environmental variables (Usage: env)

ENVIRONMENT
Language: C

OS: Ubuntu 14.04 LTS

Compiler: gcc 4.8.4

Style Guidelines: Betty style








This is our readme for our simple shell project at Holberton

Autors: Josh Beeson & Gavin Tobin
