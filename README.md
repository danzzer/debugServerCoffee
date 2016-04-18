# 使用webstorm 对server端coffee做debug

1. configurePrintScreen文件夹中为配置截图，主要注意scope中定义好文件范围（project文件夹）

2. debug PrintScreen为操作效果

3. gitignore中忽略掉project中所有的js和js.map则保证不提交这些生成的文件,写法如下

~~~
project/**/*.js
project/**/*.js.map
~~~

4. 非webstorm 的环境可以使用命令手动编译，然后使用node-inspector的方式在chrome中debug

~~~
coffee --map --compile project/
~~~
R