[ABC.html](https://github.com/user-attachments/files/26217393/ABC.html)
!DOCTYPE html>
</html>
</body>
</html>
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Bhaskara</title>
</head>

<body>
    <h1>Calcular Bhaskara</h1>

    <label>A:</label>
    <input type="number" id="a"><br><br>

    <label>B:</label>
    <input type="number" id="b"><br><br>

    <label>C:</label>
    <input type="number" id="c"><br><br>

    <button onclick="calcular()">Calcular</button>

    <p id="resultado"></p>

    <script>
        function calcular() {
            let a = Number(document.getElementById("a").value);
            let b = Number(document.getElementById("b").value);
            let c = Number(document.getElementById("c").value);

            let delta = (b * b) - (4 * a * c);

            if (delta < 0) {
                document.getElementById("resultado").innerHTML =
                    "Não possui raízes reais";
            } else {
                let x1 = (-b + Math.sqrt(delta)) / (2 * a);
                let x2 = (-b - Math.sqrt(delta)) / (2 * a);

                document.getElementById("resultado").innerHTML =
                    "Delta = " + delta + "<br>" +
                    "x1 = " + x1 + "<br>" +
                    "x2 = " + x2;
            }
        }
    </script>
</body>
</html>
