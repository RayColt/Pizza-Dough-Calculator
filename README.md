# Pizza-Dough-Calculator
Pizza Dough Calculator, just copy the html file to your phone, tabloid or computer!<br/>
<a href="https://raycolt.github.io/Pizza-Dough-Calculator">WORKING EXAMPLE</a><br/>
<img src='https://github.com/RayColt/Pizza-Dough-Calculator/blob/main/image/pdc_.jpg'/>
<script language="javascript" type="text/javascript">
function calculate(flour)
{
	if(isNaN(flour)) flour = 200;
	var fl = flour;
	var salt = 0.0075;
	var yeast = 0.015;
	var sugar = 0.03;
	var water = 0.3;
	var oil = 0.07;
	if(fl <= 0) fl = 1;
	document.getElementById("flour").value	= +fl.toFixed(4);
	document.getElementById("yeast").value	= +(fl*yeast).toFixed(4);
	document.getElementById("salt").value	= +(fl*salt).toFixed(4);
	document.getElementById("sugar").value	= +(fl*sugar).toFixed(4);
	document.getElementById("water").value	= +(fl*water).toFixed(4);//minus 30ml yeast water and oil
	document.getElementById("olive_oil").value = +(fl*oil).toFixed(4);
}
function getFlourAmount()
{
	return document.getElementById("flour").value;
}
</script>
<table width="350" border="0" cellspacing="2" cellpadding="2">
  <tr>
    <td colspan="2"><b>Pizza Dough Calculator (gr/ml)</b>🍕</td>
  </tr>
  <tr>
    <td>Flour:</td>
    <td><input style="" type="text" name="flour" id="flour" /></td>
  </tr>
  <tr>
    <td>Yeast (in 30ml water!):</td>
    <td><input type="text" name="yeast" id="yeast" disabled="disabled" /></td>
  </tr>
  <tr>
    <td>Salt:</td>
    <td><input type="text" name="salt" id="salt" disabled="disabled" /></td>
  </tr>
  <tr>
    <td>Sugar:</td>
    <td><input type="text" name="sugar" id="sugar" disabled="disabled" /></td>
  </tr>
  <tr>
    <td>Water (rest of water):</td>
    <td><input type="text" name="water" id="water" disabled="disabled" /></td>
  </tr>
  <tr>
    <td>Olive Oil:</td>
    <td><input type="text" name="olive_oil" id="olive_oil" disabled="disabled" /></td>
  </tr>
  <tr>
    <td colspan="2">let the dough rise for 1-2 hours</td>
  </tr>
  <tr>
    <td colspan="2"><input type="submit" name="submit" id="submit" value="Calculate"  onclick="calculate(parseFloat(getFlourAmount()));" /></td>
  </tr>
</table>
