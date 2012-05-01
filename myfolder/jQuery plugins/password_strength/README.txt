Jquery plugin reference : http://mypocket-technologies.com/jquery/password_strength/


STEP 1:	Include necessary files in HTML HEAD tag


<script type="text/javascript" src='http://jqueryjs.googlecode.com/files/jquery-1.3.2.min.js'></script>

<script type="text/javascript" src='password_strength.js'></script>
<link rel="stylesheet" type="text/css" href="password_strength.css">



STEP 2 : Initialize the JQuery code - change the password strength status, when the password is entered

<script>
$(document).ready( function() {

	//BASIC
	$(".password_test").passStrength({
		userid:	"#user_id"
	});
	
	//ADVANCED
	$(".password_adv").passStrength({
		shortPass: 		"top_shortPass",
		badPass:		"top_badPass",
		goodPass:		"top_goodPass",
		strongPass:		"top_strongPass",
		baseStyle:		"top_testresult",
		userid:			"#user_id_adv",			# This is important, you can simply make a hidden content with, id=user_id_adv (any where)
		messageloc:		0
	});
});
</script>



STEP 3 : Actual HTML code implementation

<!-- FOR BASIC IMAGE ICON INDICATION -->
<table cellpadding="2" cellspacing="0" border="0">
	<tr>
		<td align="right"><label>User Name:</label></td>
		<td><input type="text" name="user_name" id="user_id"/></td>
	</tr>

	<tr>
		<td align="right"><label>Password:</label></td>
		<td><input type="password" name="pass_word" class="password_test" style="float:left;"/></td>
	</tr>
</table>


<!-- FOR ADVANCED COLOR INDICATION -->
<table cellspacing="0" cellpadding="2" border="0">
	<tr>
		<td align="right"><label>User Name:</label></td>
		<td><input type="text" id="user_id_adv" name="user_name"></td>
	</tr>
	<tr>
		<td align="right"><label>Password:</label></td>
		<td><input type="password" class="password_adv" name="pass_word"></td>
	</tr>
</table>



STEP 4 : Your password strength jQuery plugin is all ready for use