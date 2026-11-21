# Portefólio infantil

Site responsivo para um portefólio infantil, com seis páginas independentes. Cada página partilha o mesmo cabeçalho, menu responsivo, seletor de idioma e rodapé. O idioma inicial é sempre Português de Portugal (`pt-PT`); Inglês e Espanhol são aplicados sem recarregar a página e só ficam guardados após um clique no seletor.

## Páginas

- `index.html`: apresentação, resumo do perfil e atalhos para as outras áreas.
- `sobre-mim.html`: história, idade, personalidade, sessões e acompanhamento parental.
- `portfolio.html`: moda infantil, retratos e sessões ao ar livre.
- `pequenas-aventuras.html`: dia a dia, passeios, brincadeiras e bastidores.
- `galeria.html`: grelha completa de fotografias.
- `contacto.html`: convites, marcas e produções mediados pelos pais.

Os seis links do menu superior apontam diretamente para estes ficheiros na raiz do projeto.

## Imagens

Substitua as imagens utilizadas mantendo os nomes e os caminhos:

- `assets/Icone.jpg`: imagem original do logótipo.
- `assets/favicon-32.png` e `assets/apple-touch-icon.png`: ícones do separador e de dispositivos móveis (32 × 32 e 180 × 180).
- `assets/social-preview.jpg`: pré-visualização Open Graph/Twitter (1200 × 630).

O logótipo com cantos arredondados também aparece na navegação: à esquerda dos links no computador e imediatamente à direita do nome no telemóvel.
- `assets/header.jpg`: imagem horizontal de fundo do cabeçalho.
- `assets/portfolio-1.jpg`, `assets/portfolio-2.jpg` e `assets/portfolio-3.jpg`: moda infantil, retratos e ar livre/estilo de vida.
- `assets/image-1.jpg` a `assets/image-8.jpg`: imagens da galeria, das histórias e da faixa animada da página inicial.

Os comentários junto às imagens em cada HTML indicam o seu papel. Os retratos usam `object-fit: cover` e `object-position` orientado para manter os rostos enquadrados. Se necessário, ajuste `object-position` no `styles.css`; o cabeçalho usa `background-position`. Os ficheiros `blog.jpg`, `service.jpg`, `client-*.jpg` e `logo-*.png` são remanescentes do template e não são utilizados.

As pré-visualizações sociais apontam para `https://zebirita.github.io/pequenas-aventuras/assets/social-preview.jpg`. Para que outros serviços consigam carregar a imagem, o site e o ficheiro têm de estar publicados num endereço público; atualize os metadados `og:url`, `og:image` e `twitter:image` se usar outro domínio.

## Textos e idiomas

Os textos da página, os textos alternativos (`alt`), títulos e meta descriptions são traduzidos em `main.js`. Para alterar ou adicionar conteúdo:

1. Adicione a mesma chave nos três objetos de idioma (`pt-PT`, `en` e `es`) em `main.js`.
2. No HTML da página, use `data-i18n="nome.da.chave"` no elemento correspondente.
3. Para traduzir um atributo em vez do texto, acrescente `data-i18n-attr="alt"` (ou `content`, `title`, `aria-label`).

Cada HTML começa com `<html lang="pt-PT">`. O site inicializa sempre em Português de Portugal mesmo que exista outro idioma em `localStorage`.

## Contacto e privacidade

O formulário em `contacto.html` recolhe nome, empresa (opcional) e propósito do trabalho, atualiza uma pré-visualização e permite escolher email ou WhatsApp. O email abre um rascunho personalizado; o WhatsApp abre uma conversa com a mensagem preenchida para o número indicado. Nenhuma mensagem é enviada automaticamente e os dados não são guardados no site. Antes de publicar, substitua `contacto-dos-pais@example.com` no atributo `action` do formulário e confirme o número WhatsApp em `main.js`. As propostas devem continuar mediadas pelos pais; evite publicar dados pessoais ou informação que identifique a criança.

## Recursos comuns

- `styles.css`: paleta, tipografia, layout e comportamento responsivo comum.
- `main.js`: traduções, seletor de idioma, menu móvel, animações e faixa de imagens.
