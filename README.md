# -> 2018948017 박범수 코딩 레포트

>#문제 1.

    a=b=c=1
    def func():
        a=b=c=2
        print("func :",a,b,c)
    print("main :",a,b,c)
    func()
    print("main :",a,b,c)
    

>#문제 2.

    a=b=c=1
    def func():
        global a,b,c
        a=b=c=2
        print("func :",a,b,c)
    print("main :",a,b,c)
    func()
    print("main :",a,b,c)
    

>#문제 3.

    a=b=c=1
    def func1():
        a=b=c=2
    def func2():
        global a,b
        a=b=3
        c=3
    print(a,b,c)
    func1()
    print(a,b,c)
    func2()
    print(a,b,c)
    

>#문제 4.

    def div_qr():
        global c,d
        c=a//b
        d=a%b
        print("몫 :",c,"나머지 :",d)
    a=int(input("정수1 : "))
    b=int(input("정수2 : "))
    div_qr()
    

>#문제 5.

    def div_qr(a,b):
        c=a//b
        d=a%b
        return(c,d)
    a=int(input("정수1 : "))
    b=int(input("정수2 : "))
    (c,d)=div_qr(a,b)
    print("몫 :",c,"나머지 :",d)
    

>#문제 6.

    data=['21','7','43','65','2','8','72','52','9']
    for i in data:
        print(i,end=" ")

>#문제 7.

    data=['21','7','43','65','2','8','72','52','9']
    a=input("찾을 값 : ")
    if a in data:
        print("위치 :",data.index(a))
    else:
        print("찾지 못함")
    

>#문제 8.

    data=[[21,7,43,65],[2,8,72,52]]
    for i in data[0]:
        print(i,end=" ")
    print("")
    for k in data[1]:
        print(k,end=" ")
    
    

> #문제 9.

    data=[['21','7','43','65'],['2','8','72','52']]
    a=input("찾을 값 : ")
    if a in data[0]:
        print("위치 : 1 행",data[0].index(a),"열")
    elif a in data[1]:
        print("위치 : 2 행",data[1].index(a),"열")
    else:
        print("찾지 못함")
    

>#문제 10.

    import copy
    s7seg_num=[[1,1,1,1,1,1,0],
               [0,1,1,0,0,0,0],
               [1,1,0,1,1,0,1],
               [1,1,1,1,0,0,1],
               [0,1,1,0,0,1,1],
               [1,0,1,1,0,1,1],
               [1,0,1,1,1,1,1],
               [1,1,1,0,0,0,0],
               [1,1,1,1,1,1,1],
               [1,1,1,1,0,1,1]]
    s7seg_num_anode=copy.deepcopy(s7seg_num)
    for i in s7seg_num:
        print(i,end=" ")
    # 10번 문제는 잘 모르겠습니다. 죄송합니다
    

>#문제 12.

    import turtle as t
    
    def up():
        t.setheading(90)
        t.forward(10)
    def down():
        t.setheading(270)
        t.forward(10)
    def right():
        t.setheading(0)
        t.forward(10)
    def left():
        t.setheading(180)
        t.forward(10)
    def home():
        t.reset()
        t.home()
