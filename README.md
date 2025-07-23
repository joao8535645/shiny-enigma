# shiny-enigma!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <title>Investigação Profunda</title>
    <style>
        body { margin: 0; background: black; display: flex; justify-content: center; align-items: center; height: 100vh; overflow: hidden; }
        #container { position: relative; width: 100%; height: 100%; display: flex; justify-content: center; align-items: center; }
        video#video-fake { width: 80%; max-width: 720px; border: 3px solid #555; }
        #susto { display: none; position: absolute; inset: 0; background: black; z-index: 10; justify-content: center; align-items: center; }
        #susto img { width: 100%; height: 100%; object-fit: cover; }
    </style>
</head>
<body>
    <div id="container">
        <video id="video-fake" autoplay muted loop>
            <source src="https://www.w3schools.com/html/mov_bbb.mp4" type="video/mp4">
            Seu navegador não suporta vídeo.
        </video>
        <div id="susto">
            <img src="https://i.imgur.com/JjGlC7P.png" alt="Susto">
            <audio id="audio-susto" autoplay>
                <source src="https://freesound.org/data/previews/341/341695_62428-lq.mp3" type="audio/mpeg">
            </audio>
        </div>
    </div>
    <script>
        setTimeout(() => {
            document.getElementById("susto").style.display = "flex";
            document.getElementById("audio-susto").play();
        }, 7000);
    </script>
</body>
</html>
