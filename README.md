# DotNetAIVoiceTranscription UI - Interface de Transcrição de Voz

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) 
![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![Visual Studio Code](https://img.shields.io/badge/VS_Code-007ACC?style=flat&logo=visual-studio-code&logoColor=white)
![Git](https://img.shields.io/badge/GIT-F05032?style=flat&logo=git&logoColor=white)

## ✨ O Backend (API) do projeto se encontra no link:

[https://github.com/marcelogmoura/DotNetAIVoiceTranscription](https://github.com/marcelogmoura/DotNetAIVoiceTranscription)

Esta é a interface de usuário (UI) desenvolvida em **React** para interagir com a API de Transcrição de Voz (DotNetAIVoiceTranscription.API). A aplicação permite que o usuário selecione um arquivo de áudio e o envie para a API, exibindo o texto transcrito em tempo real.

## 🚀 Funcionalidade Principal

O componente principal (`AudioUploader.js`) gerencia o fluxo de trabalho completo:

* **Seleção de Arquivo:** O usuário seleciona um arquivo de áudio (através do `accept="audio/*"`).
* **Upload e Transcrição:** O evento `onClick` do botão "Upload and Transcribe" dispara a função `handleUpload`, que:
    * Cria um objeto `FormData`.
    * Anexa o arquivo de áudio sob a chave `"file"`.
    * Envia a requisição `POST` para o endpoint `/transcribe` da API.
* **Exibição do Resultado:** A resposta da API (o texto transcrito) é armazenada no estado (`transcription`) e exibida na tela.

## 🛠️ Tecnologias

* **React** (`^19.2.0`)
* **Axios** (`^1.13.2`) para requisições HTTP.
* **React Scripts** (`^5.0.1`)

## ⚙️ Configuração do Projeto

### Pré-requisitos
* Node.js e npm (ou yarn).
* A API do backend (`DotNetAIVoiceTranscription.API`) deve estar rodando e acessível em `http://localhost:5075`.

### Configuração da API
O serviço HTTP (`src/Services/api.js`) está configurado com a URL base da API do backend:

```javascript
// src/Services/api.js
import axios from "axios";

const api = axios.create({
    baseURL: 'http://localhost:5075/ai',
});

export default api;
```

Se o endereço da sua API for diferente, altere o valor da **baseURL** neste arquivo.

## Como Rodar Localmente

1.  Certifique-se de que a API do backend está em execução.
2.  Navegue até o diretório do projeto:
    ```bash
    cd DotNetAIVoiceTranscription.UI
    ```
3.  Instale as dependências:
    ```bash
    npm install
    # ou yarn install
    ```
4.  Execute o projeto:
    ```bash
    npm start
    # ou yarn start
    ```
5.  A aplicação será aberta em seu navegador, geralmente em `http://localhost:3000`.


👨‍💻 **Autor:** Marcelo Moura 

📧 **Email:** [mgmoura@gmail.com](mailto:mgmoura@gmail.com)   
📧 **Email:** [admin@allriders.com.br](mailto:admin@allriders.com.br)   
🐱 **GitHub:** [github.com/marcelogmoura](https://github.com/marcelogmoura)   
🔗 **LinkedIn:** [linkedin.com/in/marcelogmoura](https://www.linkedin.com/in/marcelogmoura/)   
