**默认** 为**正常模式(normal mode)** a.k.a. 常规模式
	**正常模式(normal mode)** -> **插入模式(insert mode)**: 按**a**/**i**
	**插入模式(insert mode)** -> **正常模式(normal mode)**: 按**Esc**

**:w**: **保存(write)**: 在**正常模式(normal mode)** 下，先按**Shift+冒号(colon, :)**，光标移动到屏幕左下角；然后按**w**；最后按**回车(Return)**
	**操作(operation)**: 在**正常模式(normal mode)** 下，先按**Shift+冒号(colon, :)**，**光标(cursor)** 移动到**编辑器(editor)** 的**左下角(bottom left corner)**
	n.b. **会** **写(write)文件(file)**，**不会** **退出(quit)**

困扰世界180万程序员的难题：**如何退出 Vim**
	**:wq**: **保存并退出(write and quit)**
		**操作(operation)**: 在**正常模式(normal mode)** 下，先按**Shift+冒号(colon, :)**，**光标(cursor)** 移动到**编辑器(editor)** 的 **左下角(bottom left corner)**；然后按**wq**；最后按**回车(Return)**
		相当于**ZZ**，即在**正常模式(norma mode)** 下，连按两次**Shift+Z**
	**:q**: **退出(quit)**
		**操作(operation)**: 在**正常模式(normal mode)** 下，先按**Shift+冒号(colon, :)**，**光标(cursor)** 移动到**编辑器(editor)** 的 **左下角(bottom left corner)**；然后按**q**；最后按**回车(Return)**
		若**文件(file)** 内容**未修改**，则**直接退出(directly quit)**，**不会** **写(write)文件(file)**；若**文件(file)** 内容**已修改**，则**报错**
	**:q!**: **强制退出(force to quit)**
		**操作(operation)**: 在**正常模式(normal mode)** 下，先按**Shift+冒号(colon, :)**，**光标(cursor)** 移动到**编辑器(editor)** 的 **左下角(bottom left corner)**；然后按**q!**；最后按**回车(Return)**
		n.b. **不保存** 对**文件(file)** 内容的**修改**，**直接退出(directly quit)**，**不会** **写(write)文件(file)**
		相当于**ZQ**，即在**正常模式(normal mode)** 下，先按**Shift+Z**；后按**Shift+Q**
	**:x**: **智能退出(intelligently quit)**
		**操作(operation)**: 在**正常模式(normal mode)** 下，先按**Shift+冒号(colon, :)**，**光标(cursor)** 移动到**编辑器(editor)** 的 **左下角(bottom left corner)**；然后按**x**；最后按**回车(Return)**
		n.b. 若**文件(file)** 内容**未修改**，则**直接退出(directly quit)**，**不会** **写(write)文件(file)**，相当于 **:q**；若**文件(file)** 内容**已修改**，则**保存并退出(write and quit)**，会**写(write)文件(file)**，相当于 **:wq**
		相当于**ZZ**，即在**正常模式(normal mode)** 下，先按**Shift+冒号(colon, :)**，**光标(cursor)** 移动到**编辑器(editor)** 的**左下角(bottom left corner)**