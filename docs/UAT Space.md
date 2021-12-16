<!DOCTYPE html>
<html lang="en">
    <head>
        <!--Richard J Shelatz-->
   <head>
       <!--STYLE FOR FONT, SIZE, COLOR, CASE AND BACKGROUND(edited backgroud width to fit)-->
     </head>
   <h1>UAT Shuttle Launch!</h1>
<body>
  <img src= "https://i.ibb.co/smwX0xy/UATspace-Logo.jpg" alt= "UATspace-Logo" border= "0">
<script>
//popup enter user names
let user = prompt ("Please Enter User ID");
var userResponse;
//popup if length is over 20 "error re-enter user name must be less then 20 characters"
if (user.length >= 20){
prompt("error re-enter user name must be less then 20 characters")
}
//popup enter badge number
alert (badge = prompt ("Please Enter your Badge Number"));
var badgeResponse;
//popup if badge number is over 3 characters "error badge number must be less then 3 characters"
if (badge.length >= 4){
prompt("error re-enter your badge number must be less then 3 characters")
}
//this statment make the startButton true and the stopButton false
function StartTheCountdown() {
    document.getElementById("startButton").disabled = true;
    document.getElementById("stopButton").disabled = false;

}
//this creats a stop function, and makes the startButton false while the stopButton is true
function stop() {
    document.getElementById("startButton").disabled = false;
    document.getElementById("stopButton").disabled = true;
//this aborts the script
    document.getElementById("CountdownDisplay").innerHTML = document.write("Launch Aborted");
}

//start function
function StartTheCountdown()
{
//variable for   
var countdown = 10;
var countdownTimer = setInterval(function(){
    //if statement to display warning statment at 5 sec or less remaining
if (countdown <= 5){
document.getElementById("WarningStatment").innerHTML = "Warning Less Then 1/2 way to launch!"
}    
//if statemnet that prints blast off when clock reaches zero and just display "Blast Off!"
if (countdown == 0){    
document.getElementById("CountdownDisplay").innerHTML = document.write("Blast Off!");}
//else statement that does the count down
else {
document.getElementById("CountdownDisplay").innerHTML = countdown;}    
countdown -= 1;}, 1000);
//needs to excute on click of the stop button
function stop(){ 
document.getElementById("CountdownDisplay").innerHTML = document.write("Launch Aborted");
}
}


</script>
<!--this button was given the id startButton and excutes the StartTheCountDown function-->
<button type="button" id="startButton" onclick= "StartTheCountdown()">Launch</button>
<!--this button was given the id stopButton and excutes the stop function code-->
<button type="button" id="stopButton" onclick= "stop()">Abort!</button>
<!--this is the count down display-->
<p id="CountdownDisplay">10</p>
<!--line break-->
<br>
<!--paragraph for warning statment-->
<p2 id="WarningStatment">Launch Intilized<p2>
</body>
</html>
