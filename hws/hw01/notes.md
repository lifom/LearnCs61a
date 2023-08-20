# hw01 Notes

if_function() 
with_if_statement()
with_if_function()

三个函数取决于 cond() ture_func() false_func() 怎么设计

题目中要求的结果是:

such that with_if_statement prints the number 47, but with_if_function prints both 42 and 47.

with_if_function() 返回的结果为 if_function() ,并且将 cond() ture_func() false_func() 三个函数作为参数输入,作为参数输入时,不论结果如何,都会执行在参数中的函数,所以确定

def true_func():
    "*** YOUR CODE HERE ***"
    print(42)

def false_func():
    "*** YOUR CODE HERE ***"
    print(47)

而with_if_statement() 返回47 则需要条件为 False
所以确定

def cond():
    "*** YOUR CODE HERE ***"
    return False 