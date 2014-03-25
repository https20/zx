zx
==

file

<!-- TWO STEPS TO INSTALL COLOR ADJUSTER:

  1.  Copy the coding into the HEAD of your HTML document
  2.  Add the last code into the BODY of your HTML document  -->

<!-- STEP ONE: Paste this code into the HEAD of your HTML document  -->

<HEAD>

<SCRIPT LANGUAGE="JavaScript">
<!-- Original:  Dion (yobo42@hotmail.com) -->
<!-- Web Site:  http://www.iinet.net.au/~biab/ -->

<! >
<! >

<!-- Begin
function color(frm, clr, val) {
v = eval("0x" + frm[clr].value) + val;
if (v < 0 || v > 255) v -= val;
v = v.toString(16).toUpperCase();
while (v.length < 2) v = "0" + v;
frm[clr].value = v; nc = "";
for(i = 1; i < 8; i += 3) nc += frm.elements[i].value;
document.bgColor = nc;
}
function setval(item) {
v = prompt("New value for " + item.name + " (00 - FF)", item.value);
if (v) {
v = eval("0x" + v);
if ((v & 255) == v) {
item.value=v.toString(16).toUpperCase();
while (item.value.length < 2) item.value = "0" + item.value;
color(document.f, item.name, 0);
      }
   }
}
//  End -->
</script>
</HEAD>

<!-- STEP TWO: Copy this code into the BODY of your HTML document  -->

<BODY>

<center>
<form name=f>
<table border=1>
<tr>
<td colspan=3 align=center bgcolor="#ff0000">RED</td>
<td colspan=3 align=center bgcolor="#00ff00">GREEN</td>
<td colspan=3 align=center bgcolor="#000ff">BLUE</td>
</tr>
<tr>
<td><input type=button name=rm value="<" onclick = "color(this.form, 'Red' , -1);"></td>
<td><input type=button name=Red value="AF" onclick = "setval(this);"></td>
<td><input type=button name=rp value=">" onclick = "color(this.form, 'Red', 1);"></td>
<td><input type=button name=gm value="<" onclick = "color(this.form, 'Green', -1);"></td>
<td><input type=button name=Green value="BF" onclick = "setval(this);"></td>
<td><input type=button name=gp value=">" onclick = "color(this.form, 'Green', 1);"></td>
<td><input type=button name=bm value="<" onclick = "color(this.form, 'Blue', -1);"></td>
<td><input type=button name=Blue value="CF" onclick = "setval(this);"></td>
<td><input type=button name=bp value=">" onclick = "color(this.form, 'Blue', 1);"></td>
</tr>
</table>
</form>
</center>

 

<!-- Script Size:  2.28 KB -->
