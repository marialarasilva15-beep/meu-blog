# meu-blog
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Blog de Autoconhecimento</title>
    <style>
        /* Configurações Globais */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            color: #333;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: space-between;
        }

        /* Cabeçalho */
        header {
            text-align: center;
            padding: 40px 20px;
        }

        header h1 {
            font-size: 2.5rem;
            color: #4a5568;
            margin-bottom: 10px;
            font-weight: 600;
        }

        header p {
            color: #718096;
            font-size: 1.1rem;
        }

        /* Conteúdo Principal / Card de Frases */
        main {
            flex: 1;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 20px;
            width: 100%;
            max-width: 600px;
        }

        .quote-container {
            background: rgba(255, 255, 255, 0.85);
            backdrop-filter: blur(10px);
            padding: 40px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
            text-align: center;
            width: 100%;
            border: 1px solid rgba(255, 255, 255, 0.5);
        }

        .quote-card {
            font-size: 1.5rem;
            line-height: 1.6;
            color: #2d3748;
            font-style: italic;
            min-height: 100px;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: opacity 0.5s ease-in-out;
            opacity: 1;
        }

        .quote-card.fade-out {
            opacity: 0;
        }

        /* Rodapé */
        footer {
            width: 100%;
            text-align: center;
            padding: 20px;
            background: rgba(255, 255, 255, 0.5);
            border-top: 1px solid rgba(255, 255, 255, 0.3);
        }

        footer p {
            font-size: 0.9rem;
            color: #718096;
        }
    </style>
</head>
<body>

    <header>
        <h1>Jornada Interior</h1>
        <p>Espaço para pausar, respirar e evoluir.</p>
    </header>

    <main>
        <div class="quote-container">
            <!-- Elemento corrigido com o ID correto e frase inicial -->
            <p id="quoteText" class="quote-card">Você é a pessoa mais importante da sua própria jornada.</p>
        </div>
    </main>

    <footer> 
        <p>✨ Blog de Autoconhecimento • Transforme-se todos os dias ✨</p> 
    </footer> 

    <script> 
        const frases = [ 
            "Você é a pessoa mais importante da sua própria jornada.", 
            "Conhecer a si mesmo é o começo de toda sabedoria.", 
            "Pequenos passos geram grandes transformações.", 
            "Seu potencial é maior do que seus medos.", 
            "A mudança começa dentro de você.", 
            "Seja a melhor versão de si mesmo todos os dias." 
        ]; 
        
        let indice = 0; 
        const quoteElement = document.getElementById('quoteText');

        setInterval(() => { 
            // Inicia o efeito de sumir (fade-out)
            quoteElement.classList.add('fade-out');

            // Aguarda 500ms (tempo da transição) para trocar o texto e aparecer de novo
            setTimeout(() => {
                indice++; 
                if(indice >= frases.length){ 
                    indice = 0; 
                } 
                quoteElement.textContent = frases[indice]; 
                
                // Remove a classe para o texto reaparecer (fade-in)
                quoteElement.classList.remove('fade-out');
            }, 500);

        }, 4000); 
    </script> 
</body> 
</html>



