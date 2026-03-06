<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>鳴り響く謎</title>

<style>
body{
    background:black;
    color:white;
    text-align:center;
    font-family:sans-serif;
    margin-top:50px;
}

input{
    font-size:24px;
    width:120px;
    text-align:center;
}

button{
    font-size:20px;
    margin-left:10px;
    padding:5px 15px;
}

img{
    margin-top:30px;
    max-width:80%;
}
</style>
</head>

<body>

<h2>漢字を入力</h2>

<input id="kanjiInput" type="text" maxlength="1">
<button onclick="submitKanji()">投稿</button>

<br>

<img id="resultImage" src="images/default.png">

<script>

const imageMap = {
"僕":"images/僕.PNG",
"達":"images/達.PNG",
"弱":"images/弱.PNG",
"背":"images/背.PNG",
"中":"images/中.PNG",
"押":"images/押.PNG",
"勇":"images/勇.PNG",
"気":"images/気.PNG",
"見":"images/見.PNG",
"空":"images/空.PNG",
"綺":"images/綺.PNG",
"麗":"images/麗.PNG",
"咲":"images/咲.PNG",
"花":"images/花.PNG",
"世":"images/世.PNG",
"界":"images/界.PNG",
"優":"images/優.PNG",
"救":"images/救.PNG",
"生":"images/生.PNG",
"意":"images/意.PNG",
"味":"images/味.PNG",
"理":"images/理.PNG",
"由":"images/由.PNG",
"当":"images/当.PNG",
"前":"images/前.PNG"
};

function submitKanji(){

let input=document.getElementById("kanjiInput").value;
let img=document.getElementById("resultImage");

if(imageMap[input]){
    img.src=imageMap[input];
}else{
    img.src="images/default.png";
}

}

</script>

</body>
</html>
