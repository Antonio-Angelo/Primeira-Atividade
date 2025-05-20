# Primeira-Atividade

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="css/projeto1.css">
    <link rel="stylesheet" href="Js/jS.JS">
</head>

<body>
    
    <header>
<nav id='menu'>
  <input type='checkbox' id='responsive-menu' onclick='updatemenu()'><label></label>
  <ul>
    <img src="Imagem/expedition.jpg" alt="" width="40px" height="40px">
    <li><a href='http://'>Home</a></li>
    <li><a href='http://'>About</a></li>
    <li><a href='http://'>Contact Us</a></li>
  </ul>
</nav>

    </header>
    <br>
    <br>
    <main>
<div id="cssportal-grid">
	<div id="div1">Clair Obscur: Expedition 33 [ a ] é um RPG eletrônico baseado em turnos de 2025 desenvolvido pelo estúdio francês Sandfall Interactive e publicado pela Kepler Interactive . Ambientado em um cenário de fantasia sombria da Belle Époque , o jogo acompanha os voluntários da Expedição 33 em sua missão de destruir a Pintora, um ser que causa o Gommage anual, que apaga aqueles com idade cada vez menor. Jogado em terceira pessoa, o jogador controla um grupo de personagens, explorando áreas e se envolvendo em combate. Acoplados à sua mecânica baseada em turnos estão aspectos em tempo real, como eventos de tempo rápido e ações cronometradas em combate.</div>
	<div id="div2"><img src="quarta imagemdiv.jpg" alt="" width="150px" height="150px">
    <img src="segunda imagemdiv.jpg" alt="" width="150px" height="150px">
<img src="primeira imagemdiv.jpg" alt="" width="150px" height="150px">
<img src="terceiraimagemdiv.jpg" alt="" width="150px" height="150px"></div>
	<div id="div3"><ul>
        Nome:
        <input type="Nome">
        <br> <br> E mail:
        
        <input type="email"> <br> <br>
        Clique aqui se você não for um robô
         <input type="checkbox" id="rb1" name="rb" value="">
    </ul></div>
</div>

    </main>
    <footer></footer>
</body>
</html>

function updatemenu() {
  if (document.getElementById('responsive-menu').checked == true) {
    document.getElementById('menu').style.borderBottomRightRadius = '0';
    document.getElementById('menu').style.borderBottomLeftRadius = '0';
  }else{
    document.getElementById('menu').style.borderRadius = '10px';
  }
}



.lista{
display: block;
}
#cssportal-grid {
	display: grid;
	grid-template-rows: 1fr;
	grid-template-columns: repeat(3, 1fr);
	gap: 0;
	width: 100%;
	height: 100%;
}
#div1 {
	grid-area: 1/1/2/2;
	background-color: rgba(185,206,112, 0.5);
}
#div2 {
	grid-area: 1/2/2/3;
	background-color: rgba(65,144,34, 0.5);
}
#div3 {
	grid-area: 1/3/2/4;
	background-color: rgba(98,65,31, 0.5);
}
#menu {
	background: #0099CC;
	height: 45px;
	padding-left: 18px;
	border-radius: 10px;
}
#menu ul, #menu li {
	margin: 0 auto;
	padding: 0;
	list-style: none
}
#menu ul {
	width: 100%;
	text-align: left;
}
#menu li {
	display: inline-block;
	position: relative;
}
#menu a {
	display: block;
	line-height: 45px;
	padding: 0 14px;
	text-decoration: none;
	color: #FFFFFF;
	font-size: 16px;
}
#menu a.dropdown-arrow:after {
	content: "\25BE";
	margin-left: 5px;
}
#menu li a:hover {
	color: #0099CC;
	background: #F2F2F2;
}
#menu input {
	display: none;
	margin: 0;
	padding: 0;
	height: 45px;
	width: 100%;
	opacity: 0;
	cursor: pointer
}
#menu label {
	display: none;
	line-height: 45px;
	text-align: center;
	position: absolute;
	left: 35px
}
#menu label:before {
	font-size: 1.6em;
	color: #FFFFFF;
	content: "\2261"; 
	margin-left: 20px;
}
#menu ul.sub-menus{
	height: auto;
	overflow: hidden;
	width: 170px;
	background: #444444;
	position: absolute;
	z-index: 99;
	display: none;
}
#menu ul.sub-menus li {
	display: block;
	text-align: left;
	width: 100%;
}
#menu ul.sub-menus a {
	color: #FFFFFF;
	font-size: 16px;
}
#menu li:hover ul.sub-menus {
	display: block
}
#menu ul.sub-menus a:hover{
	background: #F2F2F2;
	color: #444444;
}
@media screen and (max-width: 800px){
	#menu {position:relative}
	#menu ul {background:#444444;position:absolute;top:100%;right:0;left:0;z-index:3;height:auto;display:none;text-align:left;}
	#menu ul.sub-menus {width:100%;position:static;}
	#menu ul.sub-menus a {padding-left:30px;}
	#menu li {display:block;float:none;width:auto;}
	#menu input, #menu label {position:absolute;top:0;left:0;display:block}
	#menu input {z-index:4}
	#menu input:checked + label {color:#FFFFFF}
	#menu input:checked + label:before {content:"\00d7"}
	#menu input:checked ~ ul {display:block}
}
