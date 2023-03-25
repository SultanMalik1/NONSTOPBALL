# NONSTOPBALL
The game involves the user trying to catch a basketball with their cursor. The basketball will move faster as the user gets closer to it, making it more challenging to catch.

<!DOCTYPE html> 
<html>

<body bgcolor=lightyellow onload="move()">

<H2>Nonstopball made by Sultan</H2>

<div id="court" onClick="move()" style="height:350px; width:700px;"> 

    <img  style="position:absolute;" src=https://rb.gy/zvu6rc>

    <span style="position:absolute; color:white;">Level - <span id="lvl">1</span>
                                              <br>Moves - <span id="mov">-1</span></span>

    <img id="ball" src=https://upload.wikimedia.org/wikipedia/commons/7/7a/Basketball.png onMouseOver="move()" onClick="resize(.95)"
         style="position:relative; width:100px;height:100px; cursor:pointer" />
</div>

<b>Click on the ball to make it smaller</b>

<script>
//--------------------------------------------------------------------------------------------
function move() 
{
    var obj = document.getElementById('ball');

    var objHeight = parseInt(obj.style.height);                     //to get rid of "px" 
    var objWidth  = parseInt(obj.style.width); 

    obj.style.top  = Math.random() * (350 - objHeight) + 'px';      //randomly place 
    obj.style.left = Math.random() * (700 - objWidth)  + 'px';      //the ball on court

    document.getElementById('mov').textContent++;                   //add 1 to number of moves 
}

function resize(ratio) 
{
    var obj = document.getElementById('ball');

    var objHeight = parseInt(obj.style.height);                     //to get rid of "px" 
    var objWidth  = parseInt(obj.style.width); 

    obj.style.height = (objHeight * ratio) + 'px';                  //make the ball smaller
    obj.style.width  = (objWidth  * ratio) + 'px';

    document.getElementById('lvl').textContent++;                   //add 1 to level number 
    document.getElementById('mov').textContent= -1;                 //reset the number of moves 
}
</script>

</body>


