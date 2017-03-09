# webservice<?php
     $db_host = "am1shyeyqbxzy8gc.cbetxkdyhwsb.us-east-1.rds.amazonaws.com";
     $db_name = "tycss4qxjg5bg48p";
     $db_user = "vscwpxgavgthv9o8";
     $db_password = "zfbx35aa3fkyakk3";
    
     $connection = mysqli_connect('am1shyeyqbxzy8gc.cbetxkdyhwsb.us-east-1.rds.amazonaws.com', 'vscwpxgavgthv9o8','zfbx35aa3fkyakk3');


     mysqli_select_db ($connection, $db_name) or die("Error al seleccionar la base de datos:".mysqli_error());
    @mysqli_query("SET NAMES 'utf8'");

$sql_query = "SELECT * FROM contactos";
$result = mysqli_query($sql_query);
$rows = array();
while($r = mysqli_fetch_assoc($result)) {
  $rows[] = $r;
}
print json_encode($rows);
?>

