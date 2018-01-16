## HTML&CSS

### 一些标签的作用
	<em> 	斜体
	<strong> 粗体
	<span>	可以提取出来，比如设置蓝色，通过在css中设置span
	<q>  	简短文本的引用，比如一句诗，会自动加双引号   
	<blockquote>	长文本的引用，会自动前后缩进
	<br /	换行
	&nbsp;	空格
	<hr /> 	分隔横线
	<address> 	斜体，地址信息
	<code> 代码标签，只能一行
	<pre>  多段代码标签

### 列表信息，在li的前面有一圆点，无序号
	<ul>
	<li>我的第一个列表信息</li> 
	</ul>
### 有序号则用ol
	<ol>
	   <li>信息</li>
	   <li>信息</li>
	   ......
	</ol>
###
	<div>  独立的逻辑  还可以增加id属性
	<div id="cool name">
### 表格
	四个元素：table tbody tr th td
	整个表格以<table>标记开始、</table>标记结束
	<tr>…</tr>：表格的一行，所以有几对tr 表格就有几行。
	<td>…</td>：表格的一个单元格，一行中包含几对<td>...</td>，说明一行中就有几列。
	<th>…</th>：表格的头部的一个单元格，表格表头。
	表格中列的个数，取决于一行中数据单元格的个数。
	比如
	<table>
	  <tbody>
	<tr>
      <th>班级</th>
      <th>学生数</th>
      <th>平均成绩</th>
    </tr>
    <tr>
      <td>一班</td>
      <td>30</td>
      <td>89</td>
    </tr>
### 默认的表格上没有边框的，需要在css式样中添加
	<style type="text/css">
	table tr td,th{border:1px solid #000;}
	</style>

	<table summary="表格简介文本">    为表格添加摘要
	<caption>标题文本</caption>      表格标题
###
	<a href="", title="",target="_blank">实际显示的蓝色文本</a>  
	链接标签，title是鼠标滑过时的文本
	target 属性是表示在新的浏览器中打开
### 发送邮件的链接
	<a href="mailto:yy@imooc.com ?subject=观了不起的盖茨比有感 
	&body=你好，对此评论有些想法。">对此影评有何感想，发送邮件给我</a>

###
	<img src="" alt="" title="提示" >    alt加载不成功时的指定文本  是一个独立的标签
###
	<form   method="传送方式"   action="服务器文件">
	HTML的表单标签，将输入的数据传送到服务器端。
	<form    method="post"   action="save.php">
        <label for="username">用户名:</label>
        <input type="text" name="username" />
        <label for="pass">密码:</label>
        <input type="password" name="pass" />
	</form>
###
	文本输入框和密码输入框
	<input type="text/password" name="名称" value="文本" />
	type="text" 文本输入框
	type="password" 密码输入框
	name是命名，提供给后台使用

### 文本输入域
	<textarea  rows="行数" cols="列数">文本</textarea>

### 单选框、复选框
	<input   type="radio/checkbox" value="值" name="名称"   checked="checked"/>
	同一框中的name必须一致，value是默认的选择

### 下拉列表框
	其中value是向服务器提交值，selected属性是显示的选项，
	<select >
	    <option value="读书">读书</option>
	    <option value="购物" selected="selected">购物</option>
	</select>
	同时multiple="multiple"可以多选
	<select multiple="multiple">

### 提交按钮
	<input   type="submit"   value="提交" name="submitBtn" />

### 重置按钮，重置表单信息,value是按钮上显示的文字
	<input type="reset" value="重置" name="btn">

### form表单中的label标签
	<label for="控件id名称">
	比如下面鼠标点击label时，就会选中单选框 他们的id必须要一致
	<label for="male">男</label>
  	<input type="radio" name="gender" id="male" />

## CSS
	比如需要将<p>我爱你</p>中的字段修改显示的样式
	则需要在head部添加style; 
	例子中 p就是选择符/选择器；{}中的就是声明；里面有属性和值；
	<style type="text/css">
	p{
	    font-size:20px;
	    color:red;
	    font-weight:blold;
	}
	</style>
	css中的注释是通过 /*xxx*/

### css样式可以出现在哪里：内联式，嵌入式，外部式三种
###
	内联式 <p style="color:red">这里文字是红色。</p>
	如果有多个属性则用分号隔开
###
	嵌入式就是在头部head style标签中
###
	外部式 就是把css代码写在一个单独的外部.css文件中
	在head标签中通过<link>标签将css文件连接到html文件内
	<link href="base.css" rel="stylesheet" type="text/css" />
	其中 rel="stylesheet" type="text/css"是固定写法
###
	如果三种方式都设置同一个标签那么 他们在相同权值的情况下的优先级：
	内联式 > 嵌入式 > 外部式

### 类选择器
	.类选择器名称{css样式代码;},比如我有一个类选择器
	.stress{color:red;}并放在<style>中
	我对<span>胆小如鼠</span>设置为stree样式则
	<span class="stress">胆小如鼠</span>

### ID选择器,跟类选择差不多
	#ID选择器名称{css样式代码;},比如我有一个ID选择器
	#stress{color:red;}并放在<style>中
	我对<span>胆小如鼠</span>设置为stree样式则
	<span id="stress">胆小如鼠</span>

>类选择器可以多个组合使用，而ID则只能使用一个 一次？？那还要它干什么？

### 子选择器
	可以将第一层标签加上样式
	.food>li{border:1px solid red;}
	.first>span{border:1px solid red;}

### 包含(后代)选择器
	所有的包含标签都作用到，用空格表示
	.food li{border:1px solid red;}

### 通用选择器，作用所有的标签
	* {color:red;}

### 伪类选择符
	比如a:hover{color:red;}，鼠标滑过时显示红色

### 分组选择符，多个标签都是同一个样式
	h1,span{color:red;}

### 多个权值叠加时，需要对某些样式设置最高权值，使用!important
	p{color:red!important;}

###元素分类
	块状元素、内联元素(又叫行内元素)和内联块状元素。

	a{display:block;} 内联元素a转换为块状元素
	块级元素独占一行
	元素的高度、宽度、行高以及顶和底边距都可设置
	元素宽度在不设置的情况下，是它本身父容器的100%
###
	display:inline  块状元素也可以设置为内联元素
	和其他元素都在一行上
	元素的高度、宽度及顶部和底部边距不可设置
	元素的宽度就是它包含的文字或图片的宽度，不可改变
###
	内联块状元素（inline-block），<img>、<input>
	display:inline-block
	和其他元素都在一行上
	元素的高度、宽度、行高以及顶和底边距都可设置

### 块元素标签都具备盒子模型
	边框 可以设置粗细、样式和颜色，比如div{border:2px  solid  red;}
	等价于
	div{
	border-width:2px;
	border-style:solid;dashed（虚线）| dotted（点线）| solid（实线）
	border-color:red;//#888
	}

	还可以为一边设置边框，其他边不设置
	div{border-bottom:1px solid red;}
	border-top:1px solid red;
	border-right:1px solid red;
	border-left:1px solid red;

	盒模型的宽和高是指内容的属性，整个模型的高和宽还需要+边界等
	div{
	    width:200px;
	    padding:20px;
	    border:1px solid red;
	    margin:10px;    
	}

### 盒模型--填充  
	元素的内容和边框之间是可以设置的
	div{padding:20px 10px 15px 30px;}  等价于
	div{
	   padding-top:20px;
	   padding-right:10px;
	   padding-bottom:15px;
	   padding-left:30px;
	}
	如果上下左右都一致可以这么些 div{padding:10px;}
	如果上下填充一样为10px，左右一样为20px div{padding:10px 20px;}

### 盒模型--边界
	元素与其它元素之间的距离可以使用边界（margin）来设置
	div{margin:20px 10px 15px 30px;}  顺序也是上右下左

### 网页的3种基本布局模型，Flow、Layer 和 Float
	
	流动模型Flow，特点
	块状元素都会在所处的包含元素内自上而下按顺序垂直延伸分布
	默认状态下，块状元素的宽度都为100%
	内联元素都会在所处的包含元素内从左到右水平分布显示

	让两个块状元素并排显示，可以用浮动模型，通过css中定义
	div{
	    width:200px;
	    height:200px;
	    border:2px red solid;
	    float:left;
	}
	<div id="div1"></div>
	<div id="div2"></div>
###
	层模型
	1、绝对定位(position: absolute)
	2、相对定位(position: relative)
	3、固定定位(position: fixed)

	绝对定位position:absolute;，相对于父包含块的位置
	div{
	    width:200px;
	    height:200px;
	    border:2px red solid;
	    position:absolute;
	    left:100px;
	    top:50px;
	}
	<div id="div1"></div>

	相对定位position:relative，相对于本来的正常位置偏移
	固定定位position:fixed;
	Relative与Absolute组合使用，使得元素块参照父元素布局
	参照定位的元素必须加入position:relative;
	#box1{
	    width:200px;
	    height:200px;
	    position:relative;        
	}
	box2相对box1的位置定位
	#box2{
	    position:absolute;
	    top:20px;
	    left:30px;         
	}

	如果top、right、bottom、left的值相同，如下面代码：
	margin:10px 10px 10px 10px;
	
	如果top和bottom值相同、left和 right的值相同，如下面代码：
	margin:10px 20px;
	
	如果left和right的值相同
	margin:10px 20px 30px;
####
	当你设置的颜色是16进制的色彩值时，如果每两位的值相同，可以缩写一半
	p{color:#000000;} = p{color: #000;}
	p{color: #336699;} = p{color: #369;}

	body{
	    font-style:italic;
	    font-variant:small-caps;
	    font-weight:bold;
	    font-size:12px;
	    line-height:1.5em;
	    font-family:"宋体",sans-serif;
	}
	缩写为
	body{
	    font:italic  small-caps  bold  12px/1.5em  "宋体",sans-serif;
	}

	1、使用这一简写方式你至少要指定 font-size 和 font-family 属性，其他的属性(如 font-weight、font-style、font-variant、line-height)如未指定将自动使用默认值。
	2、在缩写时 font-size 与 line-height 中间要加入“/”斜扛。
	有很多中文网站，这样很正常的设置
	body{
	    font:12px/1.5em  "宋体",sans-serif;
	}
###
	p{color:red;}
	p{color:rgb(133,45,200);}
	p{color:rgb(20%,33%,25%);}
	p{color:#00ffff;}
###
	长度值
	px（像素）、em、% 百分比都是相对单位
	p{font-size:12px;text-indent:2em;}
###
	水平居中设置-行内元素
	行内元素 还是 块状元素 ，块状元素里面又分为定宽块状元素，以及不定宽块状元素。

	行内元素 text-align：center
	块状元素
	定宽块状元素：块状元素的宽度width为固定值。
	定宽通过 设置左右margin来居中margin:20px auto;

	不定宽度的块状元素有三种方法居
	加入 table 标签
	设置 display: inline 方法：与第一种类似，显示类型设为 行内元素，进行不定宽元素的属性设置
	设置 position:relative 和 left:50%：利用 相对定位 的方式，将元素向左偏移 50% ，即达到居中的目的

### 垂直居中

### css中常用的属性
	{
	    font-size : 20px;
	    font-weight : normal/bold; //正常/粗体
	    font-family:"宋体";//微软雅黑Microsoft Yahei
	    font-style:italic;//斜体
	    text-decoration:underline; //下划线
	    text-decoration:line-through; //删除线
	    text-indent:2em;//文字缩进文字的2倍大小
	    line-height:2em;//行间距，行高
	    letter-spacing:50px; //文字间隔   
	    word-spacing:50px; //单词之间的间隔
	    text-align:center/left/right; //块状元素，居中
	    color : red/pink/purple/#666;  /*粉色/紫色/绿色*/
	    border:1px solid red;
	
	    display:inline-block;
		width:20px;/*在默认情况下宽度不起作用*/
		height:20px;/*在默认情况下高度不起作用*/
		background:pink;/*设置背景颜色为粉色*/
		text-align:center; /*设置文本居中显示*/
	}
