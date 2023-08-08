# Python-25-
Python学习笔记(15)
# p80 字符串的常用操作_字符串的劈分
s='hello wprld Python'
lst=s.split()
print(lst)  #劈分返回值都是列表['hello','wprld','Python']
s1='hello|world|Python'
print(s1.split(sep='|'))  #['hello','wprld','Python']
print(s1.split(sep='|',maxsplit=1))  #指定最大劈分次数，剩余的子串会单独作为一部分

‘rsplit()从右侧开始劈分’
print(s.rsplit())  #和split输出结果一样
print(s1.rsplit('|'))
print(s1.rspplit(rep='|',maxsplit=1))  #这里输出是不一样的['hello|world','Pyhon']



# p81 字符串的常用操作_字符串判断的相关方法
s='hello,python'
print('1',s.isidentifier())  #False 合法的标识符是字母数字下划线，这里的逗号不包括
print('2','hello'.isidentifier())  #True
print('3.','张三_'.isidentifier())  #True
print('4','张三_123'.isidentifier())  #True

print('5.','\t'.isspace())  #True  水平制表符是空白字符

print('6.','abc'.isalpha())  #True
print('7.','张三'.isalpha())  #True
print('8.','张三1'.isalpha())  #False 1不是字母

print('9.','123'.isdecimal())  #True
print('10.','123四'.isdecimal())  #False  四不是10进制的数字组成

print('12.','123'.isnumeric())  #True  全部由数字组成
#注：decimal的字符只有阿拉伯数字为True ，numeric函数包含较广，汉字也可以

print('15.','abcl',isalnum())  #True  全部由字母和数字组成
print('16.','张三123'.isalnum())  #True
print('17.','abc!'.isalnum())  #False  !既不是字母也不是数字



# p82 字符串的常用操作_替换与合并
s='hello,Python'
print(s.replace('Python','Java'))  #输出为hello Java
s1='hello,Python,Python,Python'
print(s1.replace('Python','Java',2))  #输出为Java,Java,Python

lst=['hello','java','Python']
print('|'.join(lst))  #输出为hello|java|Python
print(''.join(lst))  #全连在一起

t=('hello','Java','Python')  #元组用小括号
print(''.join(t))

print('*'.join('Python'))  #输出为：每个字符间插入*
