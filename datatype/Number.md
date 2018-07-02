# 数字类型
```
  注意：
  	Python3 中的数字类型存储数值，该类型是不可变的。这就意味着改变数字类型的值得话，必须重新分配内存空间。
```
## 整数 int
### 整数包括正整数和负整数。
	DEMO:
  ```
    	var_num_1 = 100
    	var_num_2 = -3
  ```

### 整数的精度
	Python3 中不区分一般整形和长整型。允许整数具有无限精度，只要内存空间允许，整数可以是无限长度的数字。
  DEMO:
  ```
      int_num = 9999999999999999999999999999999999999999999999999999999999999999999999999999999999999
      print(int_num + 1)

      # 结果为 10000000000000000000000000000000000000000000000000000000000000000000000000000000000000
  ```
  注意：Python 为了支持扩展的精度，需要做一些额外的工作，所以，长整型的运算通常要比整除的整数运算更慢。

## 浮点数 float 带有小数部分的数字或者使用科学计数法 e 或者 E
	DEMO:
  ```
    	var_num_1 = 3.14
    	var_num_2 = 3.14e-10
  ```

## 复数 complex
	DEMO:
  ```
    	var_num_1 = 3 + 4j
    	var_num_2 = 3 + 4J
  ```

  

## 布尔 bool


## 十六进制的数字
	DEMO:
  ```
	   var_num_1 = 0x9ff
  ```

## 二进制的数字
	DEMO:
  ```
	   var_num_1 = 0b10101
  ```

## 八进制的数字
	DEMO:
  ```
	   var_num_1 = 0o177
  ```

# 类型转换
	强制类型转换，譬如
  ```
    	var_num_1 = int(3.14)   # 结果为 3
    	var_num_2 = float(3)	# 结果为 3.0
  ```
	但是一般在表达式中， Python 会自动进行类型转换。

	注意：不同的类型之间，Python 不会自动进行自动转换。需要手动转换其中的某一个的类型。
	DEMO：
	string = "Python" + 3
	print(string)

	运行报错：
	Traceback (most recent call last):
	  File "D:/PythonWorkSpace/PythonABC/reLearn/DataType/Python3Number.py", line 17, in <module>
		string = "Python" + 3
	TypeError: must be str, not int

# 知识点
	1：混合类型自动升级
		举例： 40 + 3.14
		在混合类型的表达式中，Python 首先将被操作的对象转换成最复杂的操作对象对应的类型。然后再按照相同类型的操作最新进行运算。
		数字类型的复杂度：整数 > 浮点数 > 复数
