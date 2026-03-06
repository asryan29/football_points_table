<!DOCTYPE html>
<html>
<head>
<title>Football Match Table</title>

<style>

body{
font-family: Arial;
background: linear-gradient(135deg,#0f2027,#203a43,#2c5364);
color:white;
text-align:center;
padding:40px;
}

/* Creator */

.creator{
position:fixed;
top:15px;
right:20px;
background:rgba(0,0,0,0.5);
padding:6px 12px;
border-radius:20px;
font-size:14px;
}

/* Table */

table{
margin:auto;
border-collapse:collapse;
width:80%;
background:white;
color:black;
border-radius:10px;
overflow:hidden;
}

th{
background:#16a085;
color:white;
}

th,td{
padding:12px;
}

.team{
display:flex;
align-items:center;
gap:10px;
}

.team img{
width:28px;
height:28px;
}

tr{
transition:0.3s;
cursor:pointer;
}

tr:hover{
background:#e8f8f5;
transform:scale(1.01);
}

tr:nth-child(even){
background:#f4f6f6;
}

/* Modal */

.modal{
display:none;
position:fixed;
top:0;
left:0;
width:100%;
height:100%;
background:rgba(0,0,0,0.8);
justify-content:center;
align-items:center;
}

.modal-box{
background:white;
color:black;
padding:20px;
border-radius:10px;
width:90%;
max-width:450px;
}

.modal-box img{
width:80%;
margin-top:10px;
border-radius:8px;
}

.close{
float:right;
font-size:22px;
cursor:pointer;
}

</style>
</head>

<body>

<div class="creator">
Creator: Ryan
</div>

<h1>Points Table by Goal</h1>

<table>

<tr>
<th>Position</th>
<th>Player Name</th>
<th>Team</th>
<th>M</th>
<th>W</th>
<th>D</th>
<th>L</th>
<th>Pts</th>
</tr>

<tr onclick="showTeam('Santos FC','img/ss.jpg')">
<td>1</td>
<td>RyanTheChallu</td>
<td>
<div class="team">
<img src="img/santos.png">
Santos FC
</div>
</td>
<td>0</td>
<td>0</td>
<td>0</td>
<td>0</td>
<td>0</td>
</tr>

<tr onclick="showTeam('Manchester United','img/s.jpg')">
<td>2</td>
<td>Rifat Ahamad Hasan</td>
<td>
<div class="team">
<img src="img/manchester.png">
Manchester United
</div>
</td>
<td>0</td>
<td>0</td>
<td>0</td>
<td>0</td>
<td>0</td>
</tr>

</table>


<!-- Modal -->

<div id="modal" class="modal">

<div class="modal-box">

<span class="close" onclick="closeModal()">✖</span>

<h2 id="teamTitle"></h2>

<h3>Formation</h3>
<img id="formationImg">

</div>

</div>


<script>

function showTeam(name,formation){

document.getElementById("teamTitle").innerText=name;

document.getElementById("formationImg").src=formation;

document.getElementById("modal").style.display="flex";

}

function closeModal(){

document.getElementById("modal").style.display="none";

}

</script>

</body>
</html>
