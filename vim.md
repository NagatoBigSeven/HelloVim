**Vim** = **V**i **IM**proved
**Vim之父**: **布拉姆·莫勒纳尔(Bram Moolenaar)**
	墓志铭: :wq

**如何从终端(terminal)启动(start)Vim**:
```zsh
vim  # 启动(start)Vim
vim /path/to/file  # 通过Vim打开(open)文件(file)
```

**四种** **模式(mode)**:
	**正常模式(normal mode)**:
		**移动(move)**:
			**向左移动(move leftward)**: **h**
				**操作(operation)**: 在**正常模式(normal mode)** 下，按**H**
			**向下移动(move downward)**: **j**
				**操作(operation)**: 在**正常模式(normal mode)** 下，按**J**
			**向上移动(move upward)**: **k**
				**操作(operation)**: 在**正常模式(normal mode)** 下，按**K**
			**向右移动(move rightward)**: **l**
				**操作(operation)**: 在**正常模式(normal mode)** 下，按**L**
		**撤销(undo)** 与**重做(redo)**:
			**撤销(undo)**: **u**
				**操作(operation)**: 在**正常模式(normal mode)** 下，按**U**
			**重做(redo)**: **Ctrl+r**
				**操作(operation)**: 在**正常模式(normal mode)** 下，按**ctrl+R**
		**删除(delete)** **字符(character)** 或**行(line)**:
			**删除(delete)光标(cursor)所在字符(character)**: **x**
				**操作(operation)**: 在**正常模式(normal mode)** 下，按**X**
			**删除(delete)光标(cursor)所在行(r)**: **dd**
				**操作(operation)**: 在**正常模式(normal mode)** 下，连按两次**D**
		**复制粘贴(copy and paste)**:
			从**剪贴板(clipboard)** **粘贴(paste)** 到**Vim**: **"+p**
				**操作(operation)**: 在**正常模式(normal mode)** 下，先按**shift+双引号(double quote, ")/单引号(single quote, ')**；然后按**shift+加号(plus sign, +)/等号(equal sign, =)**；最后按**P**
	**插入模式(insert mode)**
	**命令模式(command mode)**
	**可视模式(visualize mode)**
	n.b. **默认** 为**正常模式(normal mode)**
**正常模式(normal mode)** -> **插入模式(insert mode)**:
		**在光标(cursor)所在字符(character)前插入(insert)**: **i**
			**操作(operation)**: 在**正常模式(normal mode)** 下，按**I**
		**在光标(cursor)所在行(line)首的第一个非空字符(character)前插入(Insert)**: **I**
			**操作(operation)**: 在**正常模式(normal mode)** 下，按**shift+I**
		**在光标(cursor)所在字符(character)后插入(append)**: **a**
			**操作(operation)**: 在**正常模式(normal mode)** 下，按**A**
		**在光标(cursor)所在行(line)尾插入(Append)**: **A**
			**操作(operation)**: 在**正常模式(normal mode)** 下，按**shift+A**
		**在光标(cursor)所在行(line)下方创建一个新行(new line)并插入(open)**: **o**
			**操作(operation)**: 在**正常模式(normal mode)** 下，按**O**
		**在光标(cursor)所在行(line)上方创建一个新行(new line)并插入(Open)**: **O**
			**操作(operation)**: 在**正常模式(normal mode)** 下，按**shift+O**
		**删除光标(cursor)所在字符(character)并插入(substitute)**: **s**
			**操作(operation)**: 在**正常模式(normal mode)** 下，按**S**
			相当于**xi**，**操作(operation)**: 在**正常模式(normal mode)** 下，先按**X**，后按**I**
		**清空光标(cursor)所在行(line)并插入(Substitute)**: **S**
			**操作(operation)**: 在**正常模式(normal mode)** 下，按**shift+S**
**正常模式(normal mode)** -> **命令模式(command mode)**: **:**
	**操作(operation)**: 在**正常模式(normal mode)** 下，按**shift+冒号(colon, :)/分号(semicolon, ;)**
**插入模式(insert mode)**/**命令模式(command mode)**/**可视模式(visualize mode)** -> **正常模式(normal mode)**: **Esc**
	**操作(operation)**: 在**插入模式(insert mode)** 下，按**esc**

**保存(write)**: **:w**
	**操作(operation)**: 在**正常模式(normal mode)** 下，先按**shift+冒号(colon, :)/分号(semicolon, ;)** 进入**命令模式(command mode)**，**光标(cursor)** 移动到**编辑器(editor)** 的**左下角(bottom left corner)**；然后按**W**；最后按**回车(return)** 执行并回到**正常模式(normal mode)**
	n.b. **会** **写(write)文件(file)**，**不会** **退出(quit)**
困扰世界180万程序员的难题：**如何退出 Vim**
	**保存并退出(write and quit)**: **:wq**
		**操作(operation)**: 在**正常模式(normal mode)** 下，先按**shift+冒号(colon, :)/分号(semicolon, ;)** 进入**命令模式(command mode)**，**光标(cursor)** 移动到**编辑器(editor)** 的 **左下角(bottom left corner)**；然后按**wq**；最后按**回车(return)** 执行并回到**正常模式(normal mode)**
		相当于**ZZ**，即在**正常模式(norma mode)** 下，连按两次**shift+Z**
	 **退出(quit)**: **:q**
		**操作(operation)**: 在**正常模式(normal mode)** 下，先按**shift+冒号(colon, :)/分号(semicolon, ;)** 进入**命令模式(command mode)**，**光标(cursor)** 移动到**编辑器(editor)** 的 **左下角(bottom left corner)**；然后按**q**；最后按**回车(return)** 执行并回到**正常模式(normal mode)**
		若**文件(file)** 内容**未修改**，则**直接退出(directly quit)**，**不会** **写(write)文件(file)**；若**文件(file)** 内容**已修改**，则**报错**
	 **强制退出(force to quit)**: **:q!**
		**操作(operation)**: 在**正常模式(normal mode)** 下，先按**shift+冒号(colon, :)/分号(semicolon, ;)** 进入**命令模式(command mode)**，**光标(cursor)** 移动到**编辑器(editor)** 的 **左下角(bottom left corner)**；然后按**q!**；最后按**回车(return)** 执行并回到**正常模式(normal mode)**
		n.b. **不保存** 对**文件(file)** 内容的**修改**，**直接退出(directly quit)**，**不会** **写(write)文件(file)**
		相当于**ZQ**，**操作(operation)**: 在**正常模式(normal mode)** 下，先按**shift+Z**；后按**shift+Q**
	**智能退出(intelligently quit)**: **:x**
		**操作(operation)**: 在**正常模式(normal mode)** 下，先按**shift+冒号(colon, :)/分号(semicolon, ;)** 进入**命令模式(command mode)**，**光标(cursor)** 移动到**编辑器(editor)** 的 **左下角(bottom left corner)**；然后按**x**；最后按**回车(return)** 执行并回到**正常模式(normal mode)**
		n.b. 若**文件(file)** 内容**未修改**，则**直接退出(directly quit)**，**不会** **写(write)文件(file)**，相当于 **:q**；若**文件(file)** 内容**已修改**，则**保存并退出(write and quit)**，会**写(write)文件(file)**，相当于 **:wq**
		相当于**ZZ**，**操作(operation)**: 在**正常模式(normal mode)** 下，连按两次**shift+Z**

**跳转到特定行号(specific line number)的行(line)首**: **:set number :<行号(line number)>**
	**操作(operation)**: 在**正常模式(normal mode)** 下，先按**shift+冒号(colon, :)/分号(semicolon, ;)** 进入**命令模式(command mode)**，**光标(cursor)** 移动到**编辑器(editor)** **左下角(bottom left corner)**；然后输入**set number**；最后按**回车(return)** 执行并回到**正常模式(normal mode)**；在**正常模式(normal mode)** 下，先按**shift+冒号(colon, :)/分号(semicolon, ;)**；然后输入**set <行号(line number)>**；最后按**回车(return)** 执行并回到**正常模式(normal mode)**

**运行(run)终端(terminal)命令(command)**: **:!<命令(command)>**
	**操作(operation)**: 在**正常模式(normal mode)** 下，按**shift+冒号(colon, :)/分号(semicolon, ;)** 进入**插入模式(insert mode)**，光标移动到**编辑器(editor)** **左下角(bottom left corner)**；然后输入 **!<命令(command)>**；最后按**回车(return)** 执行并回到**正常模式(normal mode)**

---

[![CC BY-NC-SA 4.0](https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png)](https://creativecommons.org/licenses/by-nc-sa/4.0/)