# Projeto DIO: Yu-Gi-Oh: Jo-Ken-Po Edition

Yu-Gi-Oh: Jo-Ken-Po Edition é um jogo interativo inspirado no universo de Yu-Gi-Oh, combinando a mecânica do jogo de cartas com o clássico pedra-papel-tesoura (jokenpô). Este projeto apresenta um design imersivo com elementos audiovisuais autênticos e jogabilidade dinâmica.

## 🌐Tecnologias Utilizadas

- **HTML5:** Estrutura e semântica.

- **CSS3:** Estilização e layout (incluindo um sistema customizado de botões e contêineres).

- **JavaScript (ES6+):** Lógica do jogo e manipulação de DOM.

- **Assets personalizados:** Áudios, imagens e vídeos temáticos do Yu-Gi-Oh.

#### Exemplo de Técnica Aplicada

No código abaixo, é utilizada a técnica de manipulação dinâmica do DOM para atualizar a interface de forma interativa com base na escolha do jogador e na seleção aleatória do computador:

* **Seleção dinâmica das cartas**

```javascript
function playRound(playerChoice) {
    const choices = ['pedra', 'papel', 'tesoura'];
    const computerChoice = choices[Math.floor(Math.random() * choices.length)]; 
```

* **Atualiza a interface**

```javascript
    document.getElementById('player-card').src = `./src/assets/icons/${playerChoice}.png`;
    document.getElementById('computer-card').src = `./src/assets/icons/${computerChoice}.png`;
```

* **Determina o vencedor**

```javascript
    const result = determineWinner(playerChoice, computerChoice);
    document.getElementById('result').textContent = result;
}
```

* **Função para determinar o vencedor**

```javascript
function determineWinner(player, computer) {
    if (player === computer) return 'Empate!';
    if (
        (player === 'pedra' && computer === 'tesoura') ||
        (player === 'tesoura' && computer === 'papel') ||
        (player === 'papel' && computer === 'pedra')
    ) {
        return 'Você venceu!';
    }
    return 'Você perdeu!';
}
```

Este trecho demonstra como o jogo processa as escolhas e atualiza o resultado em tempo real na interface gráfica.

## 🎮 Funcionalidades

**Jogabilidade de Jo-Ken-Po:**

* Escolha entre 3 cartas (Pedra, Papel, Tesoura) representadas por monstros clássicos do universo Yu-Gi-Oh.
* Sistema automático de seleção de cartas pelo computador.

**Sistema de pontuação:**

* Contagem de vitórias e derrotas.

* Atualização em tempo real na interface.

**Interface imersiva:**

* Vídeo de fundo temático.

* Cursor personalizado inspirado em Yu-Gi-Oh.

**Áudio temático:**

* Música de fundo e efeitos sonoros dinâmicos para vitória e derrota.

## ✨Como Jogar

**Inicie o jogo:** 
- Abra o arquivo index.html em qualquer navegador moderno.

**Escolha sua carta:** 

- Passe o mouse sobre uma carta para visualizar os detalhes e clique para selecionar.

**Duelo!:**

- A carta selecionada entra em campo.

- O computador seleciona automaticamente uma carta oponente.

- Descubra o resultado e veja a atualização de pontuação.

**Reinicie o duelo:**

- Clique no botão para começar outro round.

## 📁Estrutura do Projeto

```
Yu-Gi-Oh-JoKenPo/
├── index.html
├── src/
│   ├── assets/
│   │   ├── audios/
│   │   ├── cursor/
│   │   ├── favicon/
│   │   ├── icons/
│   │   ├── video/
│   ├── scripts/
│   │   └── engine.js
│   ├── styles/
│       ├── buttons.css
│       ├── containers_and_frames.css
│       ├── main.css
│       ├── reset.css
```

## 🔧Configuração

#### Clone este repositório:

**git clone:** 

https://github.com/RenatoMor/jogoDeCartas-yo-gi-oh.git

Certifique-se de que os arquivos estão em um diretório acessível.

Abra index.html no seu navegador.

## ⚡Personalizações

Adicionar novas cartas:

Atualize o array cardData em engine.js com novas entradas de cartas.

Inclua os ícones correspondentes no diretório ./src/assets/icons/.

Alterar áudio:

Substitua os arquivos em ./src/assets/audios/.

## 🎨Inspiração Visual

Este projeto utiliza fontes e estética retro-gaming para criar uma experiência nostálgica e imersiva, destacando a atmosfera única de Yu-Gi-Oh.

## 👨‍💻Autor

Renato Moreira


## 🔒Licença

Este projeto está licenciado sob a licença MIT. Consulte o arquivo LICENSE para mais informações.