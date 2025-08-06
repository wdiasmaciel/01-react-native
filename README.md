# 01-react-native


## Configuração do VS Code para Trabalhar com o React Native:


1) Crie uma pasta chamada ```.devcontainer``` na raiz do seu repositório no GitHub.


2) Dentro dessa pasta ```.devcontainer```, crie um arquivo chamado ```devcontainer.json```.


3) Copie e cole o conteúdo abaixo dentro do arquivo ```devcontainer.json```.
```JavaScript
// OBS: https://containers.dev/implementors/json_reference/
{
    // A imagem base para o seu Codespace. Esta imagem já vem com Node.js pré-instalado.
    // Você pode especificar uma versão específica do Node.js aqui, se preferir.
    "image": "mcr.microsoft.com/devcontainers/javascript:0-18",

    // Recursos adicionais que podem ser instalados no seu Codespace.
    // Aqui, não estamos adicionando nenhum recurso extra, pois a imagem base já é suficiente.
    "features": {
        // Exemplo: "ghcr.io/devcontainers/features/node:1": {}
    },

    // Comandos a serem executados após a criação do Codespace.
    // Usamos isso para instalar o Expo CLI globalmente.
    "postCreateCommand": "npm install -g expo-cli",

    // Configurações específicas para o VS Code dentro do Codespace.
    "customizations": {
        "vscode": {
            // Extensões do VS Code que serão automaticamente instaladas e recomendadas.
            "extensions": [
                "dbaeumer.vscode-eslint", // Para linting de código
                "esbenp.prettier-vscode", // Para formatação de código
                "msjsdiag.vscode-react-native", // Ferramentas para React Native
                "expo.vscode-expo-tools" // Ferramentas específicas para Expo
            ]
        }
    },

    // Portas que serão automaticamente encaminhadas para que você possa acessar o aplicativo.
    // O Expo usa as portas 19000 e 19001 por padrão.
    "forwardPorts": [19000, 19001],

    // Define o diretório de trabalho padrão ao abrir o terminal.
    // Isso é útil se você tiver vários projetos no mesmo repositório.
    // "workspaceFolder": "/workspaces/01-react-native", // Descomente e ajuste se necessário

    // Configurações para o terminal.
    "remoteUser": "node", // Define o usuário remoto para o container
    "containerEnv": {
        // Variáveis de ambiente que podem ser definidas no container
    }
}
```


4) Faça o ```commit``` e ```push``` dessas alterações para o seu repositório:
```
git add .
```

```
git commit -m "Arquivo de configuração para o VS Code."
```

```
git push
```

__OBS__: na próxima vez que você abrir um ```Codespace``` para este repositório, ele usará esta configuração para construir o ambiente, e você já terá o ```Expo CLI``` e as extensões prontas para usar.


## Criação de um Novo Projeto:


1) No terminal, executar o comando:
```
npx create-expo-app aplicativo
```

__OBS__: caso alguma confirmação seja exigida, digitar _yes_ (_y_).



2) Navegue para dentro da pasta criada, neste exemplo a pasta ```aplicativo```:
```Bash
cd meu-app
```


3) Depois de informar o código do aplicativo, execute o comando abaixo para executá-lo:
```
npx expo start
```
