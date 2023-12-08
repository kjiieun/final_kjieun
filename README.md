<html>
<head>
<title>LED Control</title>
</head>
<body>
LED Control:
<form method= "get" action="index.php">
<input type="submit" value="ON" name="on">
<input type="submit" value="OFF" name="off">
</form>
<?php
Ssetmode17 = shell exec("/user/local/bin/gpio -g mode 16 out");
if(isset($_GET['on'])){
Sgpio_on = shell_exec("/user/local/bin/gpio -g write 16 1");
echo "LED is on";
}
else if(isset($_GET['off'])){
Sgpio_off = shell_exec("/user/local/bin/gpio -g write 16 0");
echo "LED is off";
}
?>
</body>
</html>
