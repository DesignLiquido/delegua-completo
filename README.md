# Solução Delégua (linguagem + bibliotecas)

<br>
<p align="center">
  <img src="https://github.com/DesignLiquido/delegua/raw/principal/recursos/imagens/icone-delegua.png" alt="delegua" width="auto" height="130px">
  <h3 align="center">Linguagem Delégua</h3>

  <p align="center">
    Linguagem de programação escrita em TypeScript, derivada da <a href="https://egua.tech/docs/egua" target="_blank">Linguagem Égua</a>
  </p>

  <p align="center">
    <a href="https://designliquido.github.io/delegua-web/" target="_blank">Página Web com Interpretador Delégua para demonstrações</a>
  </p>

  <p align="center">
    <a href="https://github.com/DesignLiquido/delegua/issues" target="_blank"><img src="https://img.shields.io/github/issues/Designliquido/delegua" /></a>
    <img src="https://img.shields.io/github/stars/Designliquido/delegua" />
    <img src="https://img.shields.io/github/forks/Designliquido/delegua" />
    <a href="https://www.npmjs.com/package/delegua" target="_blank"><img src="https://img.shields.io/npm/v/delegua" /></a>
    <img src="https://img.shields.io/github/license/Designliquido/delegua" />
    <br />
  </p>

  <p align="center">
    Acompanhe a Design Líquido nas redes sociais:
  </p>
  
  <p align="center">
    <a href="https://twitter.com/designliquido" target="_blank"><img src="https://img.shields.io/static/v1?style=for-the-badge&message=Twitter&color=1DA1F2&logo=Twitter&logoColor=FFFFFF&label=" /></a>
    <a href="https://www.instagram.com/design.liquido" target="_blank"><img src="https://img.shields.io/static/v1?style=for-the-badge&message=Instagram&color=E4405F&logo=Instagram&logoColor=FFFFFF&label=" /></a>
    <a href="https://www.youtube.com/channel/UCJRn3B7r0aex6LCaOyrQtZQ" target="_blank"><img src="https://img.shields.io/static/v1?style=for-the-badge&message=YouTube&color=FF0000&logo=YouTube&logoColor=FFFFFF&label=" /></a>
    <a href="https://www.linkedin.com/company/design-liquido" target="_blank"><img src="https://img.shields.io/static/v1?style=for-the-badge&message=LinkedIn&color=0A66C2&logo=LinkedIn&logoColor=FFFFFF&label=" /></a>
    <a href="https://www.tiktok.com/@designliquido" target="_blank"><img src="https://img.shields.io/static/v1?style=for-the-badge&message=TikTok&color=000000&logo=TikTok&logoColor=FFFFFF&label=" /></a>
  </p>
</p>

Pacote da Linguagem Delégua para Node.js (NPM) com todas as blbliotecas implementadas até então:

- O núcleo da linguagem propriamente dito: https://github.com/DesignLiquido/delegua
- Biblioteca para arquivos: https://github.com/DesignLiquido/delegua-arquivos
- Biblioteca para criptografia: https://github.com/DesignLiquido/delegua-criptografia
- Biblioteca para estatística: https://github.com/DesignLiquido/delegua-estatistica
- Biblioteca para física: https://github.com/DesignLiquido/delegua-fisica
- Biblioteca para matemática: https://github.com/DesignLiquido/delegua-matematica
- Biblioteca para manejo de datas e horas: https://github.com/DesignLiquido/delegua-tempo
- Biblioteca para manejo de JSON (JavaScript Object Notation): https://github.com/DesignLiquido/delegua-json
- Biblioteca para requisições HTTP: https://github.com/DesignLiquido/delegua-http

Outra vantagem do uso deste pacote é a paridade de versões entre o núcleo e as bibliotecas. Por esta forma de instalação, todas as versões mais recentes de todas as bibliotecas de Delégua estão devidamente pareadas com a versão da linguagem em si.

## Instalação

[Você deve ter o Node.js instalado em seu ambiente](https://dicasdejavascript.com.br/instalacao-do-nodejs-e-npm-no-windows-passo-a-passo). 

Com o Node.js instalado, execute o seguinte comando em um prompt de comando (Terminal, PowerShell ou `cmd` no Windows, Terminal ou `bash` em Mac e Linux):

```bash
npm install -g delegua
```

### Usando como LAIR (Leia-Avalie-Imprima-Repita) em console

Feita a instalação no seu ambiente, execute o seguinte comando:

```sh
delegua
```

Você terá um interpretador Delégua que avalia expressões linha a linha.

Um exemplo de uso é como uma calculadora:

```js
delegua> 2 + 2
4

delegua> 2 * 3
6

delegua> 2 ** 10
1024
```

Para finalizar a execução do interpretador LAIR Delégua, use o atalho <key>Ctrl</key> + <key>C</key> (todos os sistemas operacionais).

Se quiser apenas ver a versão instalada (sem executar), use:

```sh
delegua -v
```

Ou

```sh
delegua --versao
```

Para saber os demais comandos e opções, use:

```sh
delegua --ajuda
```

#### Dialetos que suportam o modo LAIR

- Delégua
- Égua Clássico
- Pituguês

### Executando arquivos

É possível usar o interpretador com outros dialetos, como Égua.

```sh
delegua --dialeto egua
```

Ou

```sh
delegua -d pitugues
```

[Veja aqui todos os dialetos suportados](https://github.com/DesignLiquido/delegua/wiki/Dialetos).

### Executando código

É possível passar código como argumento para Delégua usando a opção `-c`:

```sh
delegua -c "escreva('Olá mundo')"
```

### Lendo código do _pipe_

```sh
echo 'escreva("Ola mundo")' | delegua -
```

## Tradução para outras linguagens

O comando geral é o seguinte:

```sh
delegua --traduzir {linguagem-origem}-para-{linguagem-destino} meu-arquivo.{extensão}
```

Exemplos:

```sh
delegua --traduzir delegua-para-javascript meu-arquivo.delegua
```
ou

```sh
delegua --traduzir javascript-para-delegua meu-arquivo.js
```

De uma forma resumida, podemos alterar o `--traduzir` para `-t`, assim como para gerar um arquivo de saída basta passar o parâmetro `--saida` ou `-s`:

```sh
delegua --traduzir delegua-para-javascript --saida meu-arquivo.delegua
```

Traduções suportadas até o momento:

- Delégua para Assembly ARM (`delegua-para-arm`) (use a opção `-a` para especificar um alvo. Padrão: `linux-arm`)
- Delégua para Assembly x64 (`delegua-para-x64`) (use a opção `-a` para especificar um alvo. Padrão: `linux`)
- Delégua para AssemblyScript (`delegua-para-assemblyscript` ou `delegua-para-as`)
- Delégua para JavaScript (`delegua-para-javascript` ou `delegua-para-js`)
- Delégua para Python (`delegua-para-python` ou `delegua-para-py`)

Traduções reversas suportadas até o momento:

- JavaScript para Delégua (`javascript-para-delegua` ou `js-para-delegua`)
- Python para Delégua (`python-para-delegua`)
- VisuAlg para Delégua (`visualg-para-delegua`)
