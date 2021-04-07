<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/
TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
//作业一，校园网注册
<meta http-equiv="Content-Type" content="text/html; charset=gb2312" />
<title></title>
</head>
<body>
<script>
//注册方法
function reg()
{
	var username = document.getElementById("username").value;
	var email = document.getElementById("email").value;
	var number = document.getElementById("number").value;
	if(document.getElementById("username").checkValidity()
	  &&document.getElementById("email").checkValidity()
	   &&document.getElementById("number").checkValidity()
	)
	{
		alert(
			'确认注册信息\n'+
			'用户名：'+username+'\n'+
			'电子邮箱：'+email+'\n'+
			'学号：'+number+'\n'
			
		)	
	}
}
</script>
<form>
<fieldset>
<legend>用户注册页面</legend>
<center>
<div style="padding:5px;width=600px">
	<h4>用户登录信息</h4>
	<table width='100%'>
		<tr>
			<td width='20%'>用户名</td>
			<td width='40%'><input id="username" type="text" required="true"  pattern="^[a-zA-Z0-9]{6,}$"/> 
            <br>
            <span  style="color:red;front-size:12px">只允许输入英文和数字，且长度至少为6位</span>
            </td>
			<td width='40%'><font color="red">*</font></td>
		</tr>
		<tr>
			<td>电子邮箱</td>
			<td><input id="email" type="email" required="true"/>
             <br>
            <span  style="color:red;front-size:12px">电子邮箱格式要符合要求</span>
            </td>
			<td><font color="red">*</font></td>
		</tr>
		<tr>
			<td>学号</td>
			<td><input id="number" type="number" required="true"/>
             <br>
            <span  style="color:red;front-size:12px">学号必须为数字</span>
            </td>
			<td><font color="red">*</font></td>
		</tr>
		
	</table>
</div>
<input type="submit" value="注册新用户" onclick="reg()">
<input type="reset" value="重置">
</center>
</fieldset>
</form>
</body>
</html>
