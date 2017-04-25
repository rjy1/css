# css
基本
<html>
	<head>
		<meta charset="utf-8" />
		<title>		
		</title>
	</head>
		
		<style type="text/css">
			*{
				margin: 0;
				padding: 0;
			}
			#box{
				width: 500px;
				height: 300px;
				border: 1px solid blue;
				margin: 0 auto;
			}
			#ul li{
				border: 1px solid red;
				width: 150px;
				height: 30px;
				list-style-type: none;
				float: left;
				line-height: 30px;
				text-align: center;
			}
			#add div{
				clear: both;
				display: none;
			}
			#uls li{
				border: 1px solid red;
				width: 150px;
				height: 30px;
				list-style-type: none;
				float: left;
				line-height: 30px;
				text-align: center;
			}
			#adds div{
				clear: both;
				display: none;
			}
		</style>
	<body>
		<div id="box">
			<ul id="ul">
				<li>1</li>
				<li>2</li>
				<li>3</li>
			</ul>
			<div id="add">
				<div style="display: block;">1</div>
				<div>2</div>
				<div>3</div>
			</div>
			<ul id="uls">
				<li>1</li>
				<li>2</li>
				<li>3</li>
			</ul>
			<div id="adds">
				<div style="display: block;">1</div>
				<div>2</div>
				<div>3</div>
			</div>
		</div>
			
		<script type="text/javascript">
			window.onload = function(){
				
				function array(name,age){
					var li = document.getElementById(name).getElementsByTagName('li'),
						div = document.getElementById(age).getElementsByTagName('div');
					
					for(var i=0;i<li.length;i++){
						li[i].index = i;				
						li[i].onclick = function(){
							for(var j=0;j<div.length;j++){
								li[j].style.background = '';
								div[j].style.display = 'none';
							}
							li[this.index].style.background = 'red';
							div[this.index].style.display = 'block';
						}
					}
				}
				array("ul",'add')
				array("uls","adds")
			}
		</script>
	</body>
</html>
