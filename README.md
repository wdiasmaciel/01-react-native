# React Native

**Autor:** Wesley Dias Maciel  
**Tema:** Introdução ao React Native

---

## Objetivo

Compreender os conceitos iniciais do React Native e construir a primeira tela com estilização.

---

## React Native

React Native é um framework criado pelo Facebook para desenvolver aplicativos móveis nativos (Android e iOS) usando **JavaScript** e **React**.  
Com ele, você escreve um único código e gera aplicativos para múltiplas plataformas.

---

## Configuração do Ambiente

### Expo CLI

#### Requisitos

- **Node.js:** [https://nodejs.org](https://nodejs.org)  
  No Linux e Codespace:
  ```bash
  sudo apt install -y nodejs
  node -v
  ```

- **Node Package Manager (NPM):**
  ```bash
  npm install -g npm@latest
  npm -v
  ```

- **Editor:** Visual Studio Code (VS Code)

- **App Expo Go:** instalar no celular Android/iOS.

---

## Criar um Projeto Usando o Expo

### Links úteis

- [Expo](https://expo.dev/)
- [Documentação do Expo](https://docs.expo.dev/)

### Comando para criar o projeto

```bash
npx create-expo-app@latest --template
```

Caso apareça a mensagem abaixo, digite `y`:

```
Need to install the following packages:
create-expo-app@3.5.3
Ok to proceed? (y)
```

- Escolha o template **blank (TypeScript)** usando as setas do teclado.
- Informe um nome para o aplicativo. Exemplo: `meu-app`

### Acesse o diretório do projeto

```bash
cd meu-app
```

### Instale dependências adicionais

```bash
npx expo install react-dom react-native-web
```

### Inicie a aplicação

```bash
npx expo start
```

Caso apareça a mensagem abaixo, digite `y`:

```
Need to install the following packages:
expo@54.0.10
Ok to proceed? (y)
```

- Pressione a tecla **"w"** para abrir a tela do aplicativo em uma nova aba do navegador.

---

## Olá, Mundo!

Abra o arquivo `App.tsx` e substitua o conteúdo por:

```tsx
import { StatusBar } from 'expo-status-bar';
import { StyleSheet, Text, View } from 'react-native';

export default function App() {
  return (
    <View style={styles.container}>
      <Text>Olá, Mundo!</Text>
      <StatusBar style="auto" />
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#fff',
    alignItems: 'center',
    justifyContent: 'center',
  },
});
```

Atualize a aba do navegador para visualizar a alteração.

> **OBS:**

### `<StatusBar style="auto" />`

- `<StatusBar style="auto" />` é um componente que controla a aparência da **barra de status superior** do dispositivo móvel.
- A barra de status exibe informações essenciais, como:
  - Hora.
  - Nível da bateria.
  - Status da rede (Wi-Fi, dados móveis).
- O atributo `style="auto"` ajusta automaticamente o estilo dos elementos internos da barra (como texto e ícones) para melhor se adequarem ao **tema claro** ou **escuro** do aplicativo, garantindo a legibilidade do conteúdo.

### `style`

- Define o estilo dos elementos dentro da barra de status.
- A opção `"auto"` adapta a cor dos ícones (claro ou escuro) com base no contraste com o fundo da barra.

### Outras propriedades comuns

- `hidden`: para **esconder** ou **exibir** a barra de status.
- `backgroundColor`: para definir a **cor de fundo** da barra, integrando-a à identidade visual do aplicativo.
- `barStyle`: permite definir explicitamente o estilo como:
  - `dark-content`
  - `light-content`
  - `default`

### Resumo

A linha:

```tsx
<StatusBar style="auto" />
```

Garante que a barra de status seja configurada com um estilo padrão que se adapta dinamicamente ao tema do seu aplicativo, mantendo o conteúdo interno legível.

---

## GitHub

Repositório do projeto: [https://github.com/wdiasmaciel/01-react-native](https://github.com/wdiasmaciel/01-react-native)

---

## Exercício

1. Atualize a mensagem do aplicativo para que ela apresente:
   - Um cumprimento com o seu nome.
   - Fundo da tela (background) na cor **vermelha**.

*Dica:* Use o estilo `backgroundColor: 'red'` e altere o texto para algo como `Olá, Ana!`
