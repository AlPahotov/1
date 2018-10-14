<!DOCTYPE html>
<html>
<head>
	<title></title>
</head>
<script type="text/javascript">
	function matrixDot (A, B) {
    var result = new Array(A.length).fill(0).map(row => new Array(B[0].length).fill(0));

    return result.map((row, i) => {
        return row.map((val, j) => {
            return A[i].reduce((sum, elm, k) => sum + (elm*B[k][j]) ,0)
        })
    })
}

var print = m => m.forEach(r => document.write(`&nbsp;&nbsp;${r.join(' ')}<br/>`)) 

var a = new Array();
a[0] = new Array();
a[0][0] = Number(prompt("Введите значение а11: ",""));
a[0][1] = Number(prompt("Введите значение a12: ",""));
a[1] = new Array();
a[1][0] = Number(prompt("Введите значение а21: ",""));
a[1][1] = Number(prompt("Введите значение a22: ",""));
var b = new Array();
b[0] = new Array();
b[0][0] = Number(prompt("Введите значение b11: ",""));
b[0][1] = Number(prompt("Введите значение b12: ",""));
b[1] = new Array();
b[1][0] = Number(prompt("Введите значение b21: ",""));
b[1][1] = Number(prompt("Введите значение b22: ",""));


document.write('matrix a:<br />');
print(a);
document.write('matrix b:<br />');
print(b);
document.write('a * b =<br />');
print(matrixDot(a,b));
</script>
<body>

</body>
</html>
