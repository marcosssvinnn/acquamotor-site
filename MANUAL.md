# Manual do Site — Acquamotor

Este documento explica como o site da Acquamotor funciona e como qualquer pessoa da equipe pode fazer alterações, com ou sem conhecimento técnico.

---

## Como o site está organizado

O site funciona com três peças conectadas:

```
Você edita os arquivos
        ↓
   GitHub (guarda o código)
        ↓
   Netlify (publica na internet automaticamente)
        ↓
   acquamotor.com.br (site no ar)
```

Sempre que alguém altera um arquivo e envia para o GitHub, o Netlify detecta a mudança e atualiza o site em menos de 1 minuto — sem precisar fazer nada manualmente.

---

## Arquivos do site

Todos os arquivos ficam na pasta `/Documents/Acquamotor/` e também no GitHub em:
**https://github.com/marcosssvinnn/acquamotor-site**

| Arquivo | O que é |
|---|---|
| `index.html` | A página inteira do site (textos, estrutura, visual) |
| `logo.png` | Logo principal que aparece no cabeçalho e rodapé |
| `favicon.svg` | Ícone pequeno que aparece na aba do navegador |
| `foto3.jpg` até `foto6.jpg` | Fotos da galeria de trabalhos |
| `video1.mp4`, `video2.mp4` | Vídeos da galeria de trabalhos |
| `equipe.jpeg` | Foto da equipe |
| `robots.txt` | Instrução para o Google sobre como indexar o site |
| `sitemap.xml` | Mapa do site para o Google |

---

## Opção 1 — Pedir mudanças pelo Claude Code (mais fácil)

Esta é a forma mais simples. Não precisa saber programar.

1. Abra o **Claude Code** no computador
2. Certifique-se de estar na pasta do projeto (`/Documents/Acquamotor`)
3. Descreva o que quer mudar em português normal, por exemplo:
   - *"Muda o número de piscinas atendidas de 1000 para 1200"*
   - *"Adiciona Porto Belo na lista de cidades da seção de contato"*
   - *"Troca a foto da galeria por essa nova aqui"*
4. O Claude edita o arquivo e faz o envio para o GitHub automaticamente
5. Em até 1 minuto o site já está atualizado

---

## Opção 2 — Editar o arquivo diretamente (requer cuidado)

Para quem quer editar sem o Claude Code.

### Passo a passo

1. Abra o arquivo `index.html` em qualquer editor de texto (Bloco de Notas, VS Code, etc.)
2. Use **Ctrl+F** (ou Cmd+F no Mac) para encontrar o texto que quer alterar
3. Faça a edição
4. Salve o arquivo
5. Envie para o GitHub (veja seção abaixo)

### O que é seguro editar

- Textos dentro de tags como `<p>`, `<h2>`, `<h3>` — são os parágrafos e títulos
- Números nas estatísticas (ex: `data-count="1000"`)
- Links do WhatsApp
- Nomes de cidades

### O que NÃO editar sem conhecimento técnico

- Linhas que começam com `<style>` — é o visual do site
- Linhas que começam com `<script>` — é o comportamento do site
- Qualquer coisa dentro de `<head>` (exceto o título da aba)

---

## Como enviar mudanças para o GitHub (publicar)

Após editar qualquer arquivo, abra o **Terminal** (ou Prompt de Comando) na pasta do projeto e execute estes três comandos em ordem:

```bash
git add .
git commit -m "Descreva aqui o que foi alterado"
git push
```

Exemplo real:
```bash
git add .
git commit -m "Atualiza número de piscinas atendidas"
git push
```

Aguarde cerca de 1 minuto e o site já estará atualizado.

---

## Como trocar fotos ou vídeos

1. Nomeie o novo arquivo **exatamente igual** ao que quer substituir (ex: `foto3.jpg`, `video1.mp4`)
2. Copie o arquivo novo para a pasta `/Documents/Acquamotor/`
3. Confirme que quer substituir quando o sistema perguntar
4. Envie para o GitHub com os comandos acima

**Formatos aceitos:**
- Fotos: `.jpg`, `.jpeg`, `.png`, `.webp`
- Vídeos: `.mp4`, `.mov`, `.webm`

---

## Como trocar o logo

1. Prepare a nova imagem com o nome `logo.png`
2. Copie para a pasta `/Documents/Acquamotor/` substituindo o arquivo antigo
3. Envie para o GitHub

O logo aparece automaticamente no cabeçalho, rodapé e nas redes sociais (WhatsApp, Google).

---

## Acessos importantes

| O quê | Onde |
|---|---|
| Site no ar | https://acquamotor.com.br |
| Código no GitHub | https://github.com/marcosssvinnn/acquamotor-site |
| Painel do Netlify | https://app.netlify.com — conta: acquamotorbc@gmail.com |
| WhatsApp do site | (47) 99630-7978 |

---

## O que fazer se algo quebrar

1. Acesse o GitHub: https://github.com/marcosssvinnn/acquamotor-site
2. Clique em **Commits** (lista de todas as alterações já feitas)
3. Encontre a última versão que estava funcionando
4. Clique em **"Revert"** para desfazer a mudança

Ou simplesmente peça ajuda pelo Claude Code descrevendo o problema.

---

## Dúvidas frequentes

**O site demorou para atualizar, o que fazer?**
Aguarde até 2 minutos. Se ainda não atualizou, acesse o painel do Netlify e veja se o deploy teve algum erro.

**Alterei o arquivo mas o site continua igual no navegador.**
Pressione **Ctrl+Shift+R** (Windows/Linux) ou **Cmd+Shift+R** (Mac) para forçar o navegador a recarregar sem cache.

**Posso editar o site pelo celular?**
Não diretamente. As edições precisam ser feitas no computador onde a pasta do projeto está salva.

**Como sei se o site está no ar normalmente?**
Acesse https://acquamotor.com.br. Se abrir, está funcionando.
