<?php
$con=mysqli_connect("localhost","root","","foodorderdb");
$un=$_POST["username"];
$pwd=$_POST["password"];
$utyp=$_GET["utype"];
$qry="select Password from  Users_tbl where UserName='$un' and UserType='$utyp'";
$result=mysqli_query($con,$qry);
while ($row=mysqli_fetch_array($result))
{
      if ($pwd==$row['Password']) 
      {
                  echo '<script> alert("Login Successful");</script>';
                  session_start();
                  $_SESSION['Uname']=$un;
                  if ($utyp=='admin')
                        header('refresh:0;url=adminLogin.php');
                  else
                        header('refresh:0;url=Dashboard.php');
      }
      else
      {
            echo '<script> alert("Incorrect UserName/User Type/Password");</script>';
            header('refresh:0;url=HomePage.html');
      }
}     
?>
