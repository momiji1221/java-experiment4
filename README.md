# java-experiment4
## 实验目的
掌握字符串String及其方法的使用
掌握文件的读取/写入方法
掌握异常处理结构
每7个汉字加入一个标点符号，奇数时加“，”，偶数时加“。”
允许提供输入参数，统计古诗中某个字或词出现的次数
输入的文本来源于文本文件B读取，把处理好的结果写入到文本文件A
考虑操作中可能出现的异常，在程序中设计异常处理程序


## 实验过程
1。使用以前的student类，稍加修改
2.创建fangfa类，import输入、输出流
3.读取文件，直到不能再读
4.将读取的文件添加标点符号，以及换行处理
5.将处理好的文件写入空白文本文档

## 核心方法
'''
   StringBuilder file1 = new StringBuilder(sbuf.toString());
			File file0 = new File("C:\\Users\\Admin\\Desktop\\文本文件A.txt");
			FileOutputStream fos = new FileOutputStream(file0);
			 int last = file1.length();
		        for(int i = 7; i <last+60 ; i+=18) {
		            file1.insert(i,'，');
		            file1.insert(i+8,'。');
		            file1.insert(i+9,'\r');
		            file1.insert(i+10,'\n');
'''

## 实验结果
实验结果正常，每行诗句都添加上了逗号和句号两个标点。

## 实验感想
java的换行方法似乎与c和python并不相同，在16个字符后（14汉字+2标点）直接输入\n并不能直接换行，在摸索下使用了
'''
                file1.insert(i+9,'\r');
		            file1.insert(i+10,'\n');
'''
这样的换行方法，才能正确换行，java的文件操作方法与python大致类似。
