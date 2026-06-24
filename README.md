meu-blog/
│
├── index.html
├── style.css
├── script.js
└── imagens/
    ├── bluetooth.png
    ├── mouse-antigo.png
    └── tecnologia.jpg
    <!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Blog de Tecnologia</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header>
        <h1>Blog de Tecnologia</h1>
    </header>

    <main>
        <article>
            <img src="imagens/tecnologia.jpg" alt="Imagem de tecnologia">
            <div>
                <h2>O Futuro da Computação</h2>
                <p class="artigo-autor">Por: Autor Principal</p>
                <p>
                    Texto da postagem sobre tecnologia e os avanços do mercado digital.
                    <br><br>
                    A evolução dos componentes melhora a experiência do usuário a cada ano.
                </p>
                <div class="botoes-container">
                    <button>❤️ <span>0</span></button>
                    <button>👍 <span>0</span></button>
                </div>
                <p class="artigo-fonte">Fonte: The National Museum of Computing</p>
            </div>
        </article>

        <article>
            <img src="imagens/mouse-antigo.png" alt="Imagem de um mouse antigo">
            <div>
                <h2>A Evolução dos Periféricos</h2>
                <p class="artigo-autor">Por: Historiador Tech</p>
                <p>Os primeiros modelos de mouse utilizavam esferas de borracha para rastrear o movimento antes do sensor óptico atual.</p>
                <div class="botoes-container">
                    <button>❤️ <span>0</span></button>
                    <button>👍 <span>0</span></button>
                </div>
                <p class="artigo-fonte">Fonte: Museu da Tecnologia</p>
            </div>
        </article>

        <article>
            <img src="imagens/bluetooth.png" alt="Imagem do Bluetooth">
            <div>
                <h2>Como Funciona o Bluetooth?</h2>
                <p class="artigo-autor">Por: Colaborador</p>
                <p>A tecnologia de rede sem fio de curto alcance revolucionou a forma como conectamos nossos periféricos diariamente.</p>
                <div class="botoes-container">
                    <button>❤️ <span>0</span></button>
                    <button>👍 <span>0</span></button>
                </div>
                <p class="artigo-fonte">Fonte: Bluetooth SIG</p>
            </div>
        </article>

        <article>
            <img src="imagens/tecnologia.jpg" alt="Tecnologia moderna">
            <div>
                <h2>Inteligência Artificial na vida moderna</h2>
                <p><strong>Subtítulo:</strong> IA transformando o cotidiano</p>
                <p class="artigo-autor">Por: Autor</p>
                <p>
                    A <strong>Inteligência Artificial</strong> está cada vez mais presente na tecnologia,
                    sendo usada em aplicativos e sistemas inteligentes.
                </p>
                <div class="botoes-container">
                    <button>❤️ <span>0</span></button>
                    <button>👍 <span>0</span></button>
                </div>
                <p class="artigo-fonte">Fonte: Materiais sobre Inteligência Artificial</p>
            </div>
        </article>
    </main>

    <script src="script.js"></script>
</body>
</html>
/* ==========================================
   RESET E CONFIGURAÇÕES GLOBAIS
   ========================================== */
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    max-width: 100vw;
    background-color: #f4f6f9;
    color: #333333;
}

/* ==========================================
   HEADER
   ========================================== */
header {
    background-color: #183C63;
    color: #FFFFFF;
    text-align: center;
    padding: 24px 16px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

header h1 {
    font-size: 2rem;
}

/* ==========================================
   LAYOUT PRINCIPAL E CARDS (FLEXBOX)
   ========================================== */
main {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 24px;
    padding: 32px 16px;
    max-width: 1200px;
    margin: 0 auto;
}

article {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    justify-content: space-between; /* Mantém os elementos alinhados verticalmente */
    border: 1px solid #e0e0e0;
    padding: 24px;
    background-color: #FFFFFF;
    border-radius: 8px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
    transition: transform 0.2s ease;
    
    /* Base de cálculo para responsividade (Cards ocupam 25% em telas grandes) */
    flex: 1 1 calc(25% - 24px); 
    min-width: 280px; /* Impede que quebrem em telas muito pequenas */
}

article:hover {
    transform: translateY(-4px);
    border-color: #183C63;
}

/* Elementos internos dos Cards */
img {
    width: 80px;
    height: 80px;
    object-fit: contain;
    margin-bottom: 16px;
}

h2 {
    font-size: 1.3rem;
    color: #183C63;
    margin-bottom: 8px;
}

.artigo-autor {
    font-weight: bold;
    font-size: 0.9rem;
    color: #555555;
    margin-bottom: 12px;
}

p {
    font-size: 1rem;
    line-height: 1.5;
    color: #444444;
}

.artigo-fonte {
    font-size: 0.8rem;
    color: #777777;
    margin-top: 16px;
    font-style: italic;
}

/* ==========================================
   BOTÕES DE INTERAÇÃO
   ========================================== */
.botoes-container {
    margin-top: 16px;
    display: flex;
    gap: 10px;
    justify-content: center;
}

button {
    background-color: #f0f4f8;
    color: #183C63;
    border: 1px solid #183C63;
    padding: 8px 16px;
    border-radius: 20px;
    cursor: pointer;
    font-size: 0.95rem;
    font-weight: bold;
    transition: all 0.2s ease;
}

button:hover {
    background-color: #183C63;
    color: #FFFFFF;
}

button span {
    margin-left: 4px;
}
// Seleciona todos os botões de reação da página (curtidas e amei)
const botoes = document.querySelectorAll("button");

// Itera sobre cada botão para isolar o seu respectivo escopo de clique
botoes.forEach(function (botao) {
    // Variável de controle individual do estado do botão
    let curtiu = false;

    botao.addEventListener("click", function () {
        // Seleciona o contador (tag span) interno deste botão específico
        let texto = botao.querySelector("span");

        if (curtiu === false) {
            texto.textContent++;
            curtiu = true;
            // Efeito visual de ativo opcional
            botao.style.backgroundColor = "#183C63";
            botao.style.color = "#FFFFFF";
        } else {
            texto.textContent--;
            curtiu = false;
            // Retorna ao estilo original
            botao.style.backgroundColor = "";
            botao.style.color = "";
        }
    });
});
