#表单标签
```
<!-- 表单域 -->
<form action="demo" method="GET" name="form1"> 
    <!-- 单行输入字段 -->
    用户名：<input type="text" name="username" value="请输入用户名" maxlength="4">     <br>
    <!-- 密码字段 -->
    密码：<input type="password" name="password">     <br>
    <!-- 单选按钮 -->
    性别：<input type="radio" name="sex" value="男" checked="checked">男     
         <input type="radio" name="sex" value="女">女     <br>
    <!-- 复选按钮 -->
    爱好：<input type="checkbox" name="hoppy" value="运动" checked="checked">运动     
         <input type="checkbox" name="hoppy" value="电影" checked="checked">电影     
         <input type="checkbox" name="hoppy" value="音乐">音乐       <br>
    <!-- 上传文件 -->
    头像：<input type="file" name>       <br>
    <!-- 提交按钮 -->
    <input type="submit">       
    <!-- 重置按钮 -->
    <input type="reset">        <br>
    <!-- 普通按钮 -->
    <input type="button">
</form>
```
##表单域
`<form>...</form>`定义表单域，提交表单的时候可以把包含的表单元素一起提交。

`action`指定后端接口，值为后端接口的url地址

`method`指定提交的方式，值为GET 或 POST

`name`指定表单的名称，当一个页面有多个表单时用于区分不同的表单

##表单元素
`<input>`单标签，定义表单元素（控件）

##表单元素的属性
###type
通过过属性值来设置控件的类型。

`type="text"`定义单行输入框

`type="password"`定义密码输入框

`type="radio"`定义单选按钮

`type="checkbox"`定义复选按钮

`type="file"`定义文件上传

`type="submit"`定义提交按钮

`type="reset"`定义重置按钮

`type="button"`定义普通按钮

###name
定义表单元素的名称，值自定义。

**对于一组单选按钮或者多选框，name的属性值必须一样**

###value
定义input输入元素的初始值，值自定义。主要是用于提交表单时向后端传值。

###checked
checked="checked"用于单选或者复选按钮，表示在首次加载时，该选项就是选中的。

###maxlength
规定输入字段的最大长度，大于这个长度则无法输入，值为正整数。

##label标签
用于绑定一个表单元素，通常和input标签一起使用，当点击label标签馁的文本时，浏览器会自动将焦点(光标)转到对应的表单元素上。

```
<label for="username">用户名：</label>
<input type="text" name="username" value="请输入用户名" maxlength="4" id="username"> 
```
```
性别：
<input type="radio" name="sex" value="男" checked="checked" id="nan">
<label for="nan">男</label>
<input type="radio" name="sex" value="女" id="nv">
<label for="nv">女</label>
```
**\<label>标签的for属性值必须和\<input>标签的id属性值一样，才构成绑定关系**