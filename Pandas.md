pandas——数据分析包
pandas两个主要的数据结构：Series和DataFrame

## Series
``` Series是一个一维数组的对象(一列)，由数据与索引组成```

- python数组转换为Series对象

```bash
$: obj = pd.Series([2,3,-5])    
   print(obj)  

>>>:  0   2   
      1   3   
      2  -5
```

- python字典转换为Series对象

```bash
$：dic = {'a':1, 'b':5, 'c':9}
   obj = pd.Series(dic)
   print(obj)

>>>: a  1
     b  5
     c  9
```

- 通过index指定索引

```bash
$: obj = pb.Series([1,5,9],index = ['a','b','c'])
   print(obj)

>>>: a  1
     b  5
     c  9
```

- 根据索引取值或赋值

```bash
$: obj['a']
>>>: 5

$: obj[['a','b']]

>>>: a  1
     c  9

```

## DataFrame
```DataFrame是一个表格型的数据结构，提供有序的列和不同类型的列值(列名-columns，行名-index)```

- 将数组转换成DataFrame对象(未指定行名)

```bash
$: data = {'name':['Alice','Bob','Eve'], 'age':[20,24,18], 'gender':['f','m','m']}
    frame = pd.DataFrame(data)
    print(frame)

>>>:   name  age  gender
0     Alice   20       f
1       Bob   24       m
2       Eve   18       m
```

- 将数组转换成DataFrame对象(指定行名)
```bash
$: data = {'name':['Alice','Bob','Eve'], 'age':[20,24,18], 'gender':['f','m','m']}
    frame = pd.DataFrame(data，index = ['p1','p2','p3'])
    print(frame)

>>>:    name   age  gender
p1     Alice    20        f
p2       Bob    24        m
p3       Eve    18        m
```
