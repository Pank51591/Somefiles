## 函数指针

### 形式1：返回类型 （*函数名）（参数表）

```c
char (*pFun)(int n);


char glFun(int a)
{
    cout << a;
    //return a;
}



int main()
{
    //将函数glFun的地址赋值给变量pFun
    pFun = glFun;
    
    //*pFun”显然是取pFun所指向地址的内容，当然也就是取出了函数glFun()的内容，然后给定参数为2。
    (*pFun)(2);
    return 0;
}
```



### 形式2： Typedef 返回类型 （*新类型） （参数表）

```c
typedef char (*PTRFUN)(int n);      //将一个函数重命名为 PTRFUN 的新类型

PTRFUN pFun;     //然后这个pFun函数就是和 PTRFUN类型函数 有相同参数的函数

char glFun(int a)
{
    return;
} 


void main() 
{ 
    //将函数glFun的地址赋值给变量pFun
    pFun = glFun; 
    
    //*pFun”显然是取pFun所指向地址的内容，当然也就是取出了函数glFun()的内容，然后给定参数为2
    (*pFun)(2); 
}




```

