# test_10_2
#include <stdio.h>
#define MaxSize 10
typedef struct{
	char data[MaxSize];
	int top;
}SqStack;
bool bracketcheck(char str[],int length){
	SqStack S;
	InitSatck(S);
	for(int i=0;i<length;i++){
		if(str[i] = "(" || str[i] = "[" || str[i] = "}"){
			Push(S,str[i]);
		}
		else{
			if(StackEmpty(S))
				return false;
			char topElem;
			Pop(S,topElem);
			if(str[i] = ")" && topElem != "(")
				return false;
			if(str[i] = "]" && topElem != "[")
				return false;
			if(str[i] = "}" && topElem != "{")
				return false;
		}
	}
	return StackEmpty(S);
}
//递归n的阶乘
int factorial(int n){
	if(n == 0 || n == 1)
		return 1;
	else
		return n*factorial(n-1);
}
//递归求斐波那契数
int Fib(int n){
	if(n == 0)
		return 0;
	else if(n == 1)
		return 1;
	else
		return Fib(n-1)+Fib(n-2);
}
int main(){
	SqStack S;
	InitStack(S);
	StackEmpty(S);
	int x = factorial(n);
	printf("%d\n",x);
	return 0;
}
