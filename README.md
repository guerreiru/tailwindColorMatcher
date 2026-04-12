# Tailwind Color Matcher

Ferramenta web simples para comparar uma cor em HEX com uma lista de cores Tailwind (em OKLCH), encontrando a mais próxima com base em distancia de cor.

## Funcionalidades

- Entrada de cor por HEX (`#rrggbb`) e color picker
- Conversao interna de `HEX -> sRGB -> OKLab -> OKLCH`
- Busca da cor mais proxima no objeto `tailwindColors`
- Exibicao de:
  - Cor de entrada
  - Melhor match
  - Top 5 correspondencias mais proximas
  - Variavel CSS sugerida (ex: `--color-red-500`)

## Estrutura do projeto

- `index.html`: arquivo principal da aplicacao
- `preview.html`: versao/rascunho da interface (se ainda estiver em uso)
- `site.webmanifest`: manifest PWA
- Icones:
  - `apple-touch-icon.png`
  - `favicon.ico`
  - `favicon-16x16.png`
  - `favicon-32x32.png`
  - `android-chrome-192x192.png`
  - `android-chrome-512x512.png`

## Como executar

Como o projeto e estatico, basta abrir o `index.html` no navegador.

Opcao recomendada (servidor local) para evitar problemas de caminho:

### Com VS Code Live Server

1. Instale a extensao Live Server
2. Clique com o botao direito em `index.html`
3. Selecione `Open with Live Server`

### Com Python

No diretorio do projeto, rode:

```bash
python -m http.server 5500
```

Depois acesse:

`http://localhost:5500`

## Personalizacao

A lista de cores usada no match esta no objeto `tailwindColors` dentro do HTML principal.

Exemplo:

```js
const tailwindColors = {
  color_red_500: "oklch(63.7% 0.237 25.331)",
  color_red_600: "oklch(57.7% 0.245 27.325)",
};
```

Para melhorar a precisao, adicione mais tons do Tailwind nesse objeto.

## Observacao sobre favicon e manifest

No estado atual, os links no `<head>` de `preview.html` apontam para `/public/...`, mas os arquivos estao na raiz do projeto.

Se os arquivos estiverem mesmo na raiz, use:

- `/apple-touch-icon.png`
- `/favicon.ico`
- `/favicon-32x32.png`
- `/favicon-16x16.png`
- `/site.webmanifest`

Se estiver usando um build tool que publica assets em `/public`, mantenha `/public/...`.

## Tecnologias

- HTML
- JavaScript vanilla
- Tailwind CSS via CDN

## Licenca

Uso livre para estudo e prototipacao. Ajuste esta secao se quiser definir uma licenca formal (MIT, Apache-2.0 etc.).
