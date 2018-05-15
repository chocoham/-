# -2018948017 박범수 입니다.

# 8-1 문제
a=input("문자열 : ")
print("문자열 길이 :", len(a))
print("첫 번째 문자 :", a[0])
print("두 번째 문자 :", a[1])
print("마지막 문자 :", a[-1])

# 8-2 문제
x=-1
a=input("문자열 : ")
for i in range(len(a)):
    x+=1
    print(a[x],end="")
print("")
y=len(a)
for k in range(len(a)):
    y-=1
    print(a[y],end="")

# 8-3 문제
score=int(input("점수 : "))
if score<=100 and score>=90:
    print(score,": A")
elif score<=89 and score>=80:
    print(score, ": B")
elif score<=79 and score>=70:
    print(score, ": C")
elif score<=69 and score>=60:
    print(score, ": D")
elif score<=59 and score>=0:
    print(score, ": F")
else:
    print("입력 가능한 점수 범위는 0~100입니다.")

# 8-4 문제
deg={10:'A',9:'A',8:'B',7:'C',6:'D',5:'F',4:'F',3:'F',2:'F',1:'F',0:'F'}
score=int(input("점수 : "))
grade=score//10
print(score, ":", deg.get(grade))

# 8-5 문제
items={"라면":650,"우유":1100,"콜라":1200,"캔커피":500,"과자":700}
a=0
sum=0
while a==0:
    it=input("제품명 : ")
    if it=="":
        break
    if it!="" and it in items:
        sum+=items.get(it)
        print("[",it,":",items.get(it),"] >", sum)
    if not it in items:
        print(it,"는 미등록 제품입니다.")
print("총 금액 :", sum)

# 8-6 문제
engkor_dict={}
eng=""
kor=""
a=0
while a==0:
    eng=input("영어 단어 : ")
    kor=input("한글 단어 : ")
    engkor_dict[eng]=kor
    if eng=="" and kor=="":
        del engkor_dict[kor]
        break
print(engkor_dict)

# 8-7 문제
engkor_dict={}
eng=""
kor=""
a=0
while a==0:
    eng=input("영어 단어 : ")
    if len(engkor_dict)==0 and eng!="":
        print("사전이 비어 있습니다.")
        print("단어를 추가합니다.")
        kor=input("한글 단어 : ")
        engkor_dict[eng]=kor
    if eng in engkor_dict:
        print(engkor_dict.get(eng))
    if not eng in engkor_dict and eng!="":
        print(eng,"단어가 등록되어 있지 않습니다.")
        print("단어를 추가합니다.")
        kor=input("한글 단어 : ")
        engkor_dict[eng]=kor
    if eng=="":
        break
print(engkor_dict)

# 8-8 문제
import time
for i in range(1,6):
    print(i,end=" ")
time.sleep(1)

# 8-9 문제
import math
num=float(input("실수 : "))
print(num,":",math.ceil(num))
print(num,":",math.floor(num))
print(num,":",math.trunc(num))
