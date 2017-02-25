
***The Path to Python: Section 2 Control Flow***
=========
# 1、条件语句
*Python条件语句是通过一条或多条语句的执行结果（True或者False）来决定执行的代码块。*

    if 判断条件：
        执行语句……
    else：
        执行语句……

    其中"判断条件"成立时（非零），则执行后面的语句，而执行内容可以多行，以缩进来区分表示同一范围。
    else 为可选语句，当需要在条件不成立时执行内容则可以执行相关语句。

# 2、循环语句

### 2.1.循环类型
Python提供了for循环和while循环（在Python中没有do..while循环）:
- while 循环：
在给定的判断条件为 true 时执行循环体，否则退出循环体。

- for 循环：
重复执行语句

- 嵌套循环：
你可以在while循环体中嵌套for循环

### 2.2. 循环控制语句

循环控制语句可以更改语句执行的顺序。Python支持以下循环控制语句：
- break 语句：
在语句块执行过程中终止循环，并且跳出整个循环
- continue 语句：
在语句块执行过程中终止当前循环，跳出该次循环，执行下一次循环。
- pass 语句：
pass是空语句，是为了保持程序结构的完整性。pass 不做任何事情，一般用做占位语句。

Test Demo:

        print('Demo 2: Difference between continue & break')
        var = 10
        while var >0:
            var -=1
            if var == 5:
                continue
            print('Current variable value : ', var)
        print('Good bye!')
        print('+' * 40)
        var = 10
        while var >0:
            var -=1
            if var == 5:
                break
            print('Current variable value : ', var)
        print('Good bye!')

Results:

        Demo 2: Difference between continue & break
        Current variable value :  9
        Current variable value :  8
        Current variable value :  7
        Current variable value :  6
        Current variable value :  4
        Current variable value :  3
        Current variable value :  2
        Current variable value :  1
        Current variable value :  0
        Good bye!
        ++++++++++++++++++++++++++++++++++++++++
        Current variable value :  9
        Current variable value :  8
        Current variable value :  7
        Current variable value :  6
        Good bye!

- else 语句： Else is introduced in python and it is placed in loop without if. It will execute only if the loop is terminated without break.

Note: there are two more else statement, one is for if that I already explained and other is with try. The difference between try else block and loop else is try else block executes when no code is executed and loop else executes when no break is executed.

*在 python 中，for … else 表示这样的意思，for 中的语句和普通的没有区别，else 中的语句会在循环正常执行完（即 for 不是通过 break 跳出而中断的）的情况下执行，while … else 也是一样。*
    # while ... else Demo
    count = 0
    while count <5:
        print(count, ' is less than 5')
        count+=1
    else:                       # while语句正常执行完后，执行else语句
        print(count, ' is not less than 5')

    # for ... else Demo
    for num in range(10, 40):
        for i in range(2, num):
            if num %i == 0:
                j = int(num / i)
                print('{0}={1} * {2}' .format(num, i, j))
                break
        else:             # i 循环正常执行完成后，执行else语句
            print(num, '是一个质数')


# 3、循环技巧

- Tips 1：在字典中循环时，关键字和对应的值可以使用 items() 方法同时解读出来。

        Person = {'Name': 'Newbigworld', 'Age': 30, 'Gender': 'Male' }
        for key, values in Person.items():
            print(key, values)
    Results:

        Gender Male
        Age 30
        Name Newbigworld

- Tips 2：在序列中循环时，索引位置和对应值可以使用 enumerate() 函数同时得到。

        for i, v in enumerate(['ID', 'Name', 'Gender', 'Age']):
            print(i, v)

    Results：

        0 ID
        1 Name
        2 Gender
        3 Age

- tips 3: 同时循环两个或更多的序列，可以使用 zip() 整体打包。

        questions = ['name', 'quest', 'favorite color']
        answers = ['lancelot', 'teh holy grail', 'blue']
        for q, a in zip(questions, answers):
            print('What is your {0}? It is {1}.'.format(q, a))

    Results:

        What is your name? It is lancelot.
        What is your quest? It is teh holy grail.
        What is your favorite color? It is blue.


- Tips 4: 需要逆向循环序列的话，先正向定位序列，然后调用 reversed() 函数。

        for i in reversed(range(1, 12, 2)):
            print(i)

    Results:

        11
        9
        7
        5
        3
        1

- Tips 5: 要按排序后的顺序循环序列的话，使用 sorted() 函数，它不改动原序列，而是生成一个新的已排序的序列。

        basket = ['apple', 'orange', 'apple', 'pear', 'orange', 'banana']
        for f in sorted(set(basket)):
            print(f)

    Results：

        apple
        banana
        orange
        pear
- Tips 6: 若要在循环内部修改正在遍历的序列（例如复制某些元素），建议您首先制作副本。在序列上循环不会隐式地创建副本。切片表示法使这尤其方便。

        words = ['cat', 'dog', 'elephant', 'defenestrate']
        for w in words[:]:
            if len(w) < 5:
                words.insert(0,w)
        print(words)

    Results:

        ['dog', 'cat', 'cat', 'dog', 'elephant', 'defenestrate']
