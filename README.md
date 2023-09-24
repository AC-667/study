# study
//凯撒密码
设想在某些情况下给朋友传递字条信息，但又不希望中途被第三方看懂这些信息，因此需要对字条信息进行加密处理。
凯撒密码是古罗马凯撒大帝用来对军事情报进行加密的算法，它采用了替换方法对信息中的每一个英文字符循环替换为字母表序列中该字符后面第三个字符，对应关系如下：
原文：ABCDEFGHIJKLMNOPQRSTUVWXYZ
密文：DEFGHIJKLMNOPQRSTUVWXYZABC
p=input()
c=' '
for i in p:
    if ord(i)<61:
        c=i
        print(c,end='')
    if ord(i)>96 and ord(i)<=119:
        c=chr(ord(i)+3)
        print(c,end='')
    if ord(i)>119:
        c=chr(ord(i)-119+96)
        print(c,end='')
//本关任务：编写程序，要求用户输入一个大写英文字母，程序根据输入字符在字母表里的顺序位置n 输出一个高度为 n 的金字塔图形，使最下面一行的中间字母是用户输入的字母。
例如，用户输入E时，程序输出如下：
//    A
//   ABA
//  ABCBA
// ABCDCBA
//ABCDEDCBA
m=input()
m=ord(m)
b=m-64
for i in range (65,m+1):
    c=i-64
    
    print((b-c)*' ',end='')
    for j in range (1,c+1):
        print(chr(64+j),end='')
    for j in range (1,c):
        print(chr(c+64-j),end='')
    print('')
//本关任务：编写一个程序，检查字符串s里是否出现单词w,如果出现，输出w,YES; 如果没有出现,输出w,NO
m=input()
n=input()
if m.find(n)==-1:
    p=n+',NO'
    print(p)
else:
    p=n+',YES'
    print(p)
//计算数字序列的和
n=int(input())
a=int(input())
s=0
t=a
while n>0:
    s=s+a
    a=a*10+t
    n=n-1
print (s)
//计算分数序列的和
n=int(input())
a=float(1)
b=float(1)
s=float(0)
while n>0:
    c=a
    a=b
    s=s+(b+c)/a
    b=b+c
    n=n-1
print ('%.3f'%s)
//分解质因数
n=int(input())
L=[]
c=n
for i in range(2,n+1):
    while 1:
        if n%i==0:
            L.append(i)
            n=n/i
        else:
            break
st=str(c)+'='
for i in L:
    st=st+str(i)+'*'
print(st[:-1])
//计算两个自然数的除法
m=input()
n=m.split(',')
s1=int(n[0])
s2=int(n[1])
s=0
a=0
while s1>s2:
    s1=s1-s2
    s=s+1
    a=s1
print(s,end='')
print(',',end='')
print(a)
