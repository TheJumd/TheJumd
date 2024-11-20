<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cuestionario de Gustos Musicales</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 20px;
            background-color: #f4f4f9;
        }
        h1 {
            text-align: center;
            color: #333;
        }
        .form-container {
            background-color: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            width: 50%;
            margin: auto;
        }
        label {
            display: block;
            margin: 10px 0 5px;
        }
        input[type="text"], input[type="radio"], select {
            width: 100%;
            padding: 8px;
            margin-bottom: 10px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        button {
            background-color: #4CAF50;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        button:hover {
            background-color: #45a049;
        }
        .result {
            margin-top: 30px;
            padding: 20px;
            background-color: #e1f7d5;
            border-radius: 8px;
            display: none;
        }
    </style>
</head>
<body>

    <h1>Cuestionario de Gustos Musicales</h1>
    <div class="form-container">
        <form id="quizForm">
            <label for="genero">¿Cuál es tu género musical favorito?</label>
            <input type="text" id="genero" name="genero" required>

            <label for="instrumento">¿Qué instrumento musical te gustaría saber tocar?</label>
            <input type="text" id="instrumento" name="instrumento" required>

            <label for="artista">¿Cuál es tu artista o banda favorita?</label>
            <input type="text" id="artista" name="artista" required>

            <label for="frecuencia">¿Con qué frecuencia escuchas música?</label>
            <select id="frecuencia" name="frecuencia" required>
                <option value="Diariamente">Diariamente</option>
                <option value="Semanalmente">Semanalmente</option>
                <option value="Rara vez">Rara vez</option>
            </select>

            <button type="button" onclick="mostrarResumen()">Enviar</button>
        </form>
    </div>

    <div class="result" id="result">
        <h2>Resumen de tus respuestas:</h2>
        <p><strong>Género musical favorito:</strong> <span id="resGeneros"></span></p>
        <p><strong>Instrumento musical que te gustaría tocar:</strong> <span id="resInstrumento"></span></p>
        <p><strong>Artista o banda favorita:</strong> <span id="resArtista"></span></p>
        <p><strong>Frecuencia con la que escuchas música:</strong> <span id="resFrecuencia"></span></p>
    </div>

    <script>
        function mostrarResumen() {
            // Obtener los valores de las respuestas del formulario
            const genero = document.getElementById("genero").value;
            const instrumento = document.getElementById("instrumento").value;
            const artista = document.getElementById("artista").value;
            const frecuencia = document.getElementById("frecuencia").value;

            // Mostrar el resumen con las respuestas
            document.getElementById("resGeneros").textContent = genero;
            document.getElementById("resInstrumento").textContent = instrumento;
            document.getElementById("resArtista").textContent = artista;
            document.getElementById("resFrecuencia").textContent = frecuencia;

            // Mostrar el div con el resumen
            document.getElementById("result").style.display = "block";
        }
    </script>

</body>
</html>
