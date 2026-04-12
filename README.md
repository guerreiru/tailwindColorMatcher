# Tailwind Color Matcher

Ferramenta web para comparar uma cor em HEX com a paleta Tailwind em OKLCH e encontrar o melhor match.

## Funcionalidades

- Entrada de cor por HEX (`#rrggbb`) e color picker
- Conversão interna de `HEX -> sRGB -> OKLab -> OKLCH`
- Busca da cor mais próxima no conjunto `tailwindColors`
- Exibição da cor de entrada, melhor match, top 5 resultados e variável CSS sugerida

## Estrutura do projeto

- `index.html`: interface e lógica principal da aplicação
- `tailwindColors.js`: objeto com a paleta de cores em OKLCH
- `site.webmanifest`: manifest PWA

Ícones na raiz do projeto:

- `apple-touch-icon.png`
- `favicon.ico`
- `favicon-16x16.png`
- `favicon-32x32.png`
- `android-chrome-192x192.png`
- `android-chrome-512x512.png`

## Como executar

Como o projeto é estático, você pode abrir `index.html` direto no navegador. A opção recomendada é usar servidor local.

### VS Code Live Server

1. Instale a extensão Live Server.
2. Clique com o botão direito em `index.html`.
3. Selecione `Open with Live Server`.

### Python

No diretório do projeto, execute:

```bash
python -m http.server 5500
```

Depois acesse `http://localhost:5500`.

## Personalização

A lista de cores usada no match está em `tailwindColors.js`.

Exemplo:

```js
const tailwindColors = {
  color_red_500: "oklch(63.7% 0.237 25.331)",
  color_red_600: "oklch(57.7% 0.245 27.325)",
};
```

Para melhorar a precisão, adicione mais tons do Tailwind nesse objeto.

## Favicon e Manifest

No estado atual do projeto, os arquivos estão na raiz. Portanto, os links no `<head>` devem usar:

- `/apple-touch-icon.png`
- `/favicon.ico`
- `/favicon-32x32.png`
- `/favicon-16x16.png`
- `/site.webmanifest`

## Tecnologias

- HTML
- JavaScript (Vanilla)
- Tailwind CSS via CDN

## Licença

Uso livre para estudo e prototipação. Ajuste esta seção se quiser adotar uma licença formal (por exemplo, MIT).
