# Gerador de Thumbnail

Aplicação web para montar cards de 1200 x 630 px, formato usado em capas de LinkedIn, imagens Open Graph e apresentações. A edição acontece no navegador e a exportação gera um PNG nas dimensões exatas.

[![GitHub Pages](https://img.shields.io/badge/Deploy-GitHub%20Pages-blue?logo=github)](https://samuel-c-santos.github.io/gerador-de-thumbnail/)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)

Ferramenta publicada em https://samuel-c-santos.github.io/gerador-de-thumbnail/

## Como funciona

O card é um elemento de tamanho fixo (1200 x 630 px). Na prévia ele é reduzido com `transform: scale()` para caber na coluna, mas o layout interno permanece em 1200 x 630. A exportação usa o elemento em tamanho real com html2canvas, então o PNG não depende do tamanho da janela nem do zoom do navegador.

## Recursos

**Texto**

- Título, etiqueta e subtítulo editáveis.
- Redução automática do tamanho da fonte quando o texto passa do espaço disponível.
- Etiqueta vazia esconde o elemento.

**Cores**

- Fundo, destaque, texto, subtítulo e ícones, por seletor de cor ou hexadecimal.
- Oito paletas prontas e uma rampa de cores de destaque.
- Bordas, sombras e a cor do texto da etiqueta são calculados a partir do contraste das cores escolhidas.

**Fontes**

- Nove opções: Archivo, Space Grotesk, Inter, Manrope, Poppins, Montserrat, Source Sans 3, Merriweather e JetBrains Mono.

**Foto**

- Upload de imagem com recorte quadrado, usando Cropper.js.

**Tecnologias**

- 85 itens em seis grupos: dados, bancos, geo, web, cloud e design.
- Busca por nome ou grupo, ignorando acentos.
- Até cinco ícones no card.
- Ferramentas sem ícone no FontAwesome são exibidas com monograma (DDB, QG, PG).

**Exportação**

- PNG em 1200 x 630.
- Nome do arquivo gerado a partir do título.

**Privacidade**

- O processamento é local. Nenhum arquivo ou dado é enviado para servidor.

## Limitações

- O layout do card é fixo: texto à esquerda, foto à direita, sem posicionamento livre dos elementos.
- Tema, textos e tecnologias ficam apenas na memória da página. Recarregar a página volta aos valores padrão.

## Exemplos

| Samuel Santos, tema laranja | Samuel Santos, tema verde | Elen Camila, tema rosa |
|:---:|:---:|:---:|
| ![Samuel Santos, tema laranja](samuel-santos-thumbnail.png) | ![Samuel Santos, tema verde](samuel-santos-thumbnail-2.png) | ![Elen Camila, tema rosa](elen-camila-thumbnail.png) |

## Uso local

```bash
git clone https://github.com/samuel-c-santos/gerador-de-thumbnail.git
cd gerador-de-thumbnail
```

Abra o `index.html` no navegador ou sirva a pasta:

```bash
npx serve .
```

Não existe etapa de build nem dependência para instalar.

## Estrutura

```
index.html                       aplicação completa (interface, card e exportação)
samuel-santos-thumbnail.png      exemplo
samuel-santos-thumbnail-2.png    exemplo
elen-camila-thumbnail.png        exemplo
LICENSE                          licença MIT
README.md
```

## Dependências

Bibliotecas carregadas por CDN, sem gerenciador de pacotes:

- html2canvas 1.4.1
- Cropper.js 1.6.1
- Font Awesome 6.4
- Google Fonts

## Licença

MIT. Consulte [LICENSE](LICENSE).
