<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aplicación de Denuncias de Violencia</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 20px;
            background-color: #f0f0f0;
        }
        .container {
            max-width: 600px;
            margin: 0 auto;
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        h1 {
            color: #333;
            text-align: center;
        }
        form {
            margin-top: 20px;
        }
        label {
            display: block;
            margin-bottom: 5px;
            color: #555;
        }
        input, textarea, select {
            width: 100%;
            padding: 10px;
            margin-bottom: 15px;
            border: 1px solid #ddd;
            border-radius: 4px;
            box-sizing: border-box;
        }
        button {
            background-color: #4CAF50;
            color: white;
            padding: 12px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            width: 100%;
            font-size: 16px;
        }
        button:hover {
            background-color: #45a049;
        }
        #mensajes {
            margin-top: 20px;
            padding: 10px;
            border-radius: 4px;
        }
        .exito {
            background-color: #d4edda;
            color: #155724;
            border: 1px solid #c3e6cb;
        }
        .error {
            background-color: #f8d7da;
            color: #721c24;
            border: 1px solid #f5c6cb;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Sistema de Denuncias de Violencia</h1>
        <form id="denunciaForm">
            <label for="nombre completo">Nombre completo:</label>
            <input type="text" id="nombre completo" name="nombre completo">

            <label for="email">Correo electrónico:</label>
            <input type="email" id="email" name="email">

            <label for="tipo">Tipo de violencia:</label>
            <select id="tipo" name="tipo" required>
                <option value="">Seleccione un tipo</option>
                <option value="fisica">Física</option>
                <option value="psicologica">Psicológica</option>
                <option value="sexual">Sexual</option>
                <option value="economica">Económica</option>
                <option value="doméstica">Doméstica</option>
                <option value="escolar">Escolar</option>
                <option value="laboral">Laboral</option>
                <option value="social">Social</option>
                <option value="otro">Otro</option>
            </select>

            <label for="lugar">Lugar del incidente:</label>
            <input type="text" id="lugar" name="lugar" required>

            <label for="fecha">Fecha del incidente:</label>
            <input type="date" id="fecha" name="fecha" required>

            <label for="descripcion">Descripción de la situación:</label>
            <textarea id="descripcion" name="descripcion" rows="5" required></textarea>

            <button type="submit">Enviar Denuncia</button>
        </form>

        <div id="mensajes"></div>
    </div>

    <script src="app.js"></script>
</body>
</html>
