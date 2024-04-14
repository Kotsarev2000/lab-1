# lab-1
<!doctype html>
<html lang="en">
 <head>
  <link rel="stylesheet" type="text/css" href="styles.css">
 </head>
 <body>
<div id="MyClockDisplay" class="clock" onload="showTime()">
  <script src="clock.js"></script>
</div>

 

<div class="wrapper clearfix">
  <div class="left">

    <div class="name-hero">

     

      <div class="name-text">
       
        <h1>Kotsarev <em>Maksim</em></h1>
        <p>Cherkasy, 18000</p>
        <p>mkotsarev90@gmail.com</p>
        <p>0970863968</p>

      </div>

    </div>

  </div>
  <div class="right">

    <div class="inner">
      <section>
        <h1>Education</h1>
        <p><em><b>Old Kovray secondary school</b></em></p>
        <p>Cherkasy oblast, Old Kovray, Ukraine
        </p>
        <p>September 2010 - June 2021
</p>
        <p><b>Сompleted general secondary education</b></p>
        <p><em><b>Cherkasy State Technological University</b></em></p>
        <p>Cherkasy, Ukraine</p>
        <p>Sep 2021 - Present</p>
      </section>
      <section>
        <h1>Technical Skills</h1>
        <ul class="skill-set">
          <li>Mobile Development</li>
          <li>Python</li>
          <li>HTML5</li>
          <li>CSS3</li>
          <li>JS</li>
          <li>C++</li>
          <li>C#</li>
        </ul>
      </section>
      <section>
        <h1>Experience</h1>
        <p><em><b>Study in Cherkasy State Technological University
</b></em></p>
        <p>Sep 2021 - Present</p>
        <p><em><b>Mate academy</b></em></p>
        <p>Front-end developer</p>
        <p>2020 April - 2020 August</p>
      </section>
      <section>
        <h1>Personal Interests</h1>
        <ul class="skill-set">
          <li>Futures trading</li>
          <li>Voleyball</li>
          <li>Runing</li>
          <li>Reading</li>
          <li>Tennis</li>
        </ul>
      </section>
      <section>
        
      </section>
    </div>

  </div>

</div>
</body>
</html>
CSS
*, *:before, *:after {
  -moz-box-sizing: border-box; -webkit-box-sizing: border-box; box-sizing: border-box;
 }
html
{
	font-size:100%;
}
body
{
	-webkit-font-smoothing:antialiased;
	color:#333332;
	font-family:Lora, serif;
	font-size:18px;
	font-weight:400;
	line-height:1.4;
	text-rendering:optimizeLegibility;
}
h1
{
	color:rgba(0,0,0,.75);
}
.wrapper
{
	height:100%;
}
.left
{
	background-color:rgba(0,0,0,.025);
	border-right:1px solid rgba(0,0,0,.05);
	float:right;
	height:100%;
	margin-left:-1px;
	min-width:256px;
	position:fixed;
	width:33.33%;
}
.right
{
	float:right;
	height:100%;
	position:relative;
	width:66.66%;
}
.name-hero
{
	background:rgba(0,0,0,.001);
	bottom:0;
	height:290px;
	left:0;
	margin:auto;
	position:absolute;
	right:0;
	top:0;
	width:85%;
}

.name-hero h1
{
	font-family:Open Sans, sans-serif;
	font-size:1.5em;
	text-align:center;
}

.name-hero h1 em
{
	color:rgba(0,0,0,.3);
	font-style:normal;
	font-weight:700;
}
.name-hero p
{
	color:rgba(0,0,0,.75);
	font-size:.75em;
	line-height:1.5;
	margin:0 8px 0 0;
	text-align:center;
}
.name-hero .name-text
{
	margin:0 auto;
	width:85%;
}
.inner
{
	margin:0 auto;
	max-width:975px;
	padding:3em;
}

.inner h1
{
	font-size:1.75em;
}

.inner p
{
	color:rgba(0,0,0,.5);
}

.inner p em
{
	color:rgba(0,0,0,1);
	font-style:normal;
}

.inner section
{
	margin:100px auto;
}

ul
{
	list-style-type:none;
	margin-top:-10px;
	max-width:570px;
	padding:0;
}
.skill-set li
{
	background:rgba(0,0,0,.75);
	border-radius:5px;
	color:#FFF;
	list-style:none;
	margin:15px 15px 0 0;
	padding:10px;
  text-align:justify;
}

.handmade {
  text-align:right;
  margin-top:100px;
}
.handmade em {
  font-family: 'Shadows Into Light', cursive;
  font-size: 1.25em;
  margin-left:5px;
}
.clock {
    position: absolute;
    top: 5%;
    left: 96%;
    transform: translateX(-50%) translateY(-50%);
    color: #000000;
    font-size: 20px;
    font-family: Orbitron;
    letter-spacing: 7px;

JS
function showTime(){
    var date = new Date();
    var h = date.getHours(); // 0 - 23
    var m = date.getMinutes(); // 0 - 59
    var s = date.getSeconds(); // 0 - 59
    var session = "AM";
    
    if(h == 0){
        h = 12;
    }
    
    if(h > 12){
        h = h - 12;
        session = "PM";
    }
    
    h = (h < 10) ? "0" + h : h;
    m = (m < 10) ? "0" + m : m;
    s = (s < 10) ? "0" + s : s;
    
    var time = h + ":" + m + ":" + s + " " + session;
    document.getElementById("MyClockDisplay").innerText = time;
    document.getElementById("MyClockDisplay").textContent = time;
    
    setTimeout(showTime, 1000);
    
}

showTime();
