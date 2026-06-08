## 检查
	try-expect:
		1.PermissionError错误
			对文件使用：
			try:
				items = list(path.iterdir())
			except PermissionError:
				print("没有权限读取这个文件夹")
				return None
				
				核心是用pah.iterdir()方法（返回一个迭代器，不真正遍历目录）创
				建路径下的遍历对象，再使用list()方法展开为列表，强制访问这些对
				象，再用try-expect捕获错误

## 模块 
参照[python官方页面](https://www.python.org/):
	[parhlib](https://docs.pythonlang.cn/3/library/pathlib.html#basic-use):
		1.功能：此模块提供表示文件系统路径的类，其语义适用于不同的操作系统
		2.语法：
			(1)path.parent # 所在文件夹
			(2)path.stem # 主文件名：example
			(3)info.st_size # 文件大小，单位是字节
			(4)info.st_mtime # 最后修改时间，时间戳格式
			(5)relative_to() # 把绝对路径或完整路径转换成相对路径
	[shutil](https://docs.python.org/zh-cn/3/library/shutil.html):
		1.功能：python用于复制文件的模块
		2.语法：
			（1）Shutil.copy2 () 方法用于将源文件的内容复制到目标文件或目录
	[csv](https://docs.python.org/zh-cn/3/library/csv.html):
		1.功能：# CSV 文件读写
		2.语法：
			（1）csv.writer 返回一个 writer 对象，该对象负责将用户的数据在给定
			的文件型对象上转换为带分隔符的字符串。

## 内置函数
参照[python官方页面](https://www.python.org/):
	 [open(_file_, _mode='r'_, _buffering=-1_, _encoding=None_, _errors=None_, _newline=None_, _closefd=True_, _opener=None_)](https://docs.python.org/zh-cn/3/library/functions.html#open):
		1.功能：打开一个文件，并返回一个文件对象，能通过接收实参从读取和写入模式中
		切换
	[next()](https://docs.python.org/zh-cn/3/library/functions.html#next):
		1.功能：通过调用 [iterator](https://docs.python.org/zh-cn/3/glossary.html#term-iterator) 的 [`__next__()`](https://docs.python.org/zh-cn/3/library/stdtypes.html#iterator.__next__ "iterator.__next__") 方法获取下一个元素。如果迭代器耗尽，则返回给定的 _default_，如果没有默认值则触发 [`StopIteration`](https://docs.python.org/zh-cn/3/library/exceptions.html#StopIteration "StopIteration")。
	