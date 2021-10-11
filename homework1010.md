#homework 10.10
####2021级经济学院国际商务2班 
####贾培桐 22021039994
***


	def func(nums,month):
		if month<3:
			return nums*(month+1)
		a=b=nums
		for i in range(2,month):
			result=a+b
			a,b=b,result
		return result+a+b
	
	print(func(2, 12))

```flow
st=>start: 开始
op=>operation: 输入初始兔子数量、目标月份
op2=>operation: 当月可生育兔子数量等于前两个月可生育兔子数量之和,i+1
return1=>operation: 返回兔子数量(目标月份少于三个月不构成斐波那契数列)
return2=>operation: 返回兔子数量(当月可生育兔子数量*2+上个月可生育兔子数量)
cond1=>condition: 目标月份是否小于三个月?
cond2=>condition: i=2,i小于目标月份？
e=>end
st->op->cond1
cond1(yes)->return1
cond1(no)->cond2
cond2(yes)->op2->cond2
cond2(no)->return2
return1->e
return2->e
```
