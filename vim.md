**Vim** = **V**i **IM**proved
**Vim之父**: **布拉姆·莫勒纳尔(Bram Moolenaar)**

**如何启动(start)Vim**:
```zsh
vim  # 启动(start)Vim
vim /path/to/file  # 通过Vim打开(open)文件(file)
```

**四种** **模式(mode)**:
	**正常模式(normal mode)**:
		**撤销(undo)**: **u**
			**操作(operation)**: 在**正常模式(normal mode)** 下按**U**
		**重做(redo)**: **Ctrl+r**
			**操作(operation)**: 在**正常模式(normal mode)** 下按**ctrl+R**
	**插入模式(insert mode)**
	**命令模式(command mode)**
	**可视模式(visualize mode)**
	n.b. **默认** 为**正常模式(normal mode)**
**正常模式(normal mode)** -> **插入模式(insert mode)**:
		**在光标所在字符前插入(insert)**: **i**
			**操作(operation)**: 在**正常模式(normal mode)** 下按**O**
		**在光标所在行首的第一个非空字符前插入(Insert)**: **I**
			**操作(operation)**: 在**正常模式(normal mode)** 下按**shift+I**
		**在光标所在字符后插入(append)**: **a**
			**操作(operation)**: 在**正常模式(normal mode)** 下按**A**
		**在光标所在行尾插入(Append)**: **A**
			**操作(operation)**: 在**正常模式(normal mode)** 下按**shift+A**
		**在光标所在行下方创建一个新行并插入(open)**: **o**
			**操作(operation)**: 在**正常模式(normal mode)** 下按**O**
		**在光标所在行上方创建一个新行并插入(Open)**: **O**
			**操作(operation)**: 在**正常模式(normal mode)** 下按**shift+O**
		**替换光标所在的字符(substitute)**: **s**
			**操作(operation)**: 在**正常模式(normal mode)** 下按**S**
		**替换光标所在行(Substitute)**: **S**
			**操作(operation)**: 在**正常模式(normal mode)** 下按**shift+S**
	**插入模式(insert mode)** -> **正常模式(normal mode)**: 在**插入模式(insert mode)** 下按**esc**

**保存(write)**: **:w**
	**操作(operation)**: 在**正常模式(normal mode)** 下，先按**shift+分号(semicolon, ;)/冒号(colon, :)** 进入**命令模式(command mode)**，**光标(cursor)** 移动到**编辑器(editor)** 的**左下角(bottom left corner)**
	n.b. **会** **写(write)文件(file)**，**不会** **退出(quit)**

困扰世界180万程序员的难题：**如何退出 Vim**
	**保存并退出(write and quit)**: **:wq**
		**操作(operation)**: 在**正常模式(normal mode)** 下，先按**shift+分号(semicolon, ;)/冒号(colon, :)**，**光标(cursor)** 移动到**编辑器(editor)** 的 **左下角(bottom left corner)**；然后按**wq**；最后按**回车(return)**
		相当于**ZZ**，即在**正常模式(norma mode)** 下，连按两次**shift+Z**
	 **退出(quit)**: **:q**
		**操作(operation)**: 在**正常模式(normal mode)** 下，先按**shift+分号(semicolon, ;)/冒号(colon, :)**，**光标(cursor)** 移动到**编辑器(editor)** 的 **左下角(bottom left corner)**；然后按**q**；最后按**回车(return)**
		若**文件(file)** 内容**未修改**，则**直接退出(directly quit)**，**不会** **写(write)文件(file)**；若**文件(file)** 内容**已修改**，则**报错**
	 **强制退出(force to quit)**: **:q!**
		**操作(operation)**: 在**正常模式(normal mode)** 下，先按**shift+分号(semicolon, ;)/冒号(colon, :)**，**光标(cursor)** 移动到**编辑器(editor)** 的 **左下角(bottom left corner)**；然后按**q!**；最后按**回车(return)**
		n.b. **不保存** 对**文件(file)** 内容的**修改**，**直接退出(directly quit)**，**不会** **写(write)文件(file)**
		相当于**ZQ**，即在**正常模式(normal mode)** 下，先按**shift+Z**；后按**shift+Q**
	**智能退出(intelligently quit)**: **:x**
		**操作(operation)**: 在**正常模式(normal mode)** 下，先按**shift+分号(semicolon, ;)/冒号(colon, :)**，**光标(cursor)** 移动到**编辑器(editor)** 的 **左下角(bottom left corner)**；然后按**x**；最后按**回车(return)**
		n.b. 若**文件(file)** 内容**未修改**，则**直接退出(directly quit)**，**不会** **写(write)文件(file)**，相当于 **:q**；若**文件(file)** 内容**已修改**，则**保存并退出(write and quit)**，会**写(write)文件(file)**，相当于 **:wq**
		相当于**ZZ**，即在**正常模式(normal mode)** 下，先按**shift+分号(semicolon, ;)/冒号(colon, :)**，**光标(cursor)** 移动到**编辑器(editor)** 的**左下角(bottom left corner)**