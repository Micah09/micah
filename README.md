<!-- Created by Tapabrata Banerjee [Studying - No DM] [Busy] -->
<!-- Created by Namu Micah -->



<!DOCTYPE HTML>
<html>
<head>
  <title> Our Daily Bread </title>
</head>
<body bgcolor="gray">
<form>
<font size="0">
<h1><center><font face="Times New Roman" color="white" size="50">OUR DAILY BREAD</font></center></h1>
<center><font face="Times New Roman" size="5">Membership form </font></center>
<pre>FIRST NAME:  <input type="text" size="25" id="fN"/></pre>
<pre>MIDDLE NAME: <input type="text" size="25" id="mN"/></pre>
<pre>LAST NAME:   <input type="text" size="25" id="lN"/></pre>
<pre>PHONE NO:    <input type="text" size="25" id="pN"/></pre>
<pre>EMAIL:       <input type="text" size="25" placeholder="example@gmail.com" id="eL"/></pre> GENDER:
<input type="radio" name="sex" value="MALE" class="gD">MALE </input>
<input type="radio" name="sex" value="FEMALE" class="gD">FEMALE </input><br>
<pre>ACTIVE ROLES: <br>
<input class="aR" type="checkbox" value="TO SHARE"/>TO SHARE</input><br>
<input class="aR" type="checkbox" value="TO EDIT"/>TO EDIT </input><br>
<input class="aR" type="checkbox" value="TO SPONSOR"/>TO SPONSOR</input></pre>
<br><pre>STATE: <select name="dropdown" id="sT">
<option value="ABIA">ABIA</option>
<option value="ADAMAWA">ADAMAWA</option>
<option value="AKWA">AKWA IBOM</option>
<option value="ANAMBRA">ANAMBRA</option>
<option value="BAUCHI">BAUCHI</option>
<option value="BAYELSA">BAYELSA</option>
<option value="BENUE">BENUE</option>
<option value="BORNO">BORNO</option>
<option value="CROSS RIVER">CROSS RIVER</option>
<option value="DELTA">DELTA</option>
<option value="EBONYI">EBONYI</option>
<option value="EDO">EDO</option>
<option value="EKITI">EKITI</option>
<option value="ENUGU">ENUGU</option>
<option value="GOMBE">GOMBE</option>
<option value="IMO">IMO</option>
<option value="JIGAWA">JIGAWA</option>
<option value="KADUNA">KADUNA</option>
<option value="KANO">KANO</option>
<option value="KATSINA">KATSINA</option>
<option value="KEBI">KEBBI</option>
<option value="KOGI">KOGI</option>
<option value="KWARA">KWARA</option>
<option value="LAGOS">LAGOS</option>
<option value="NASARAWA">NASARAWA</option>
<option value="NIGER">NIGER</option>
<option value="OGUN">OGUN</option>
<option value="ONDO">ONDO</option>
<option value="OSUN">OSUN</option>
<option value="OYO">OYO</option>
<option value="PLATEAU">PLATEAU</option>
<option value="RIVERS">RIVERS</option>
<option value="SOKOTO">SOKOTO</option>
<option value="TARABA">TARABA</option>
<option value="YOBE">YOBE</option>
<option value="ZAMFARA">ZAMFARA</option>
<option value="ABUJA">ABUJA</option></pre>
</select>
<pre>COUNTRY: <input type="text" size="20" id="cT"/></pre>
<br><input type="RESET" value="RESET"/>
<br><strong><a onclick = 'send()'><font size="5">SUBMIT</font></a></strong><br>
<font face="Times New Roman" color="black" size="4"><strong>ABOUT OUR DAILY BREAD</strong> </font>
<font face="Times New Roman" color="white" size="3"><em><font size="0">Our Daily Bread is a non denominational
daily spiritual diet for the soul.
It is so rich that it addresses
every area of one's life. It was
founded on the 6th of July 2020.
It was a burden in my heart that
gave birth to our daily bread but
today our daily bread is being read
in other countries. The very foundation
of our daily bread is in Matthew 6:11
"Give us this day our daily bread."
The daily bread represent daily grace,
strength, power, VISION and encouragement
as we daily walk with GOD. I implore you
in the name of GOD to eat this spiritual
diet and share with others on daily basis.
Join us as we reach the online audience
with the daily short write up. Your
spiritual welfare is my concern.</em>

<strong>Namu Joel.
General Coordinator, Our Daily Bread.</strong></font>
<br><font size="5"><marquee><font face="Times New Roman" color="green">JESUS <font face="Times New Roman" color="white">IS </font> <font face="Times New Roman" color="green">LORD </font></marquee></font>
</font>
</font>
</form>
</body>
</html>
// Created by Tapabrata Banerjee [Studying - No DM] [Busy]


// Created by Namu Micah
var firstName, middleName, lastName, phNo, email, gender, genderCheck, genderVal, genderValue, activeRoles, activeRoleCheck, activeRoleValue, activeRoleVal , country, text;
function send()
{
    firstName = document.getElementById("fN").value;
    middleName = document.getElementById("mN").value;
    lastName = document.getElementById("lN").value;
    phNo = document.getElementById("pN").value;
    email = document.getElementById("eL").value;
    gender = document.querySelectorAll(".gD");
    genderCheck =  [gender[0].checked,  gender[1].checked];
    genderVal = [gender[0].value,  gender[1].value];
    for(let j = 0; j < gender.length; j++)
    {
        if(genderCheck[j])
        {
            genderValue = genderVal[j];
        }
    }
    activeRoles = document.querySelectorAll(".aR");
    activeRoleCheck =  [activeRoles[0].checked,  activeRoles[1].checked, activeRoles[2].checked];
    activeRoleVal = [activeRoles[0].value,  activeRoles[1].value, activeRoles[2].value];
    activeRoleValue = "";
    for(let i = 0; i < activeRoles.length; i++)
    {
        if(activeRoleCheck[i])
        {
        if(i==0)
            activeRoleValue =  activeRoleVal[i];
        }
        else
        {
            activeRoleValue = activeRoleValue + ", " + activeRoleVal[i];
        }
    }
    state = document.getElementById("sT").value;
    country = document.getElementById("cT").value;
    text = "First Name:" + firstName + "; " + "Middle Name:" + middleName + "; " + "Last Name:" + lastName + "; " + "Phone Number: " + phNo + "; " + "Email: " + email + "; " + "Gender: " + gender + "; " + "Active Roles: " + activeRoleValue + "; " + "State: " + state + "; " + "Country: " + country;
    window.open("http://wa.me/+2348153553960?text=" + text, "_blank").focus()
}
