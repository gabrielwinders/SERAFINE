# Serafine — site institucional

Site de página única da Serafine, loja de moda masculina no centro histórico
de Diamantina, Minas Gerais.

HTML e CSS puros, sem build, sem dependências. É só abrir o `index.html`.

---

## Arquivos

```
index.html                 o site inteiro (HTML + CSS + JS em um arquivo só)
favicon.svg                ícone da aba, a pena da marca em ouro
img/serafine-logo.png      logo com fundo transparente
img/og-image.png           imagem de preview ao compartilhar o link (1200×630)
.nojekyll                  desliga o processamento Jekyll do GitHub Pages
```

---

## Publicar no GitHub Pages

1. Crie um repositório novo no GitHub chamado `serafine`, público.
2. Envie os arquivos. Pela interface do site: **Add file → Upload files**,
   arraste tudo e clique em **Commit changes**.
   Importante: arraste os arquivos soltos, não a pasta zipada, e mantenha a
   pasta `img` com o mesmo nome.
3. Vá em **Settings → Pages**.
4. Em **Source**, escolha `Deploy from a branch`; em **Branch**, escolha
   `main` e a pasta `/ (root)`. Salve.
5. Espere de um a dois minutos. O endereço fica:
   `https://SEU-USUARIO.github.io/serafine/`

Pela linha de comando, se preferir:

```bash
git init
git add .
git commit -m "Primeira versão do site"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/serafine.git
git push -u origin main
```

Depois é só ativar o Pages pelo passo 3 acima.

---

## Antes de mandar o link para alguém

Abra o `index.html` e troque `SEU-USUARIO` pelo seu usuário do GitHub nas
quatro linhas de metatag que têm esse texto. São elas que fazem o WhatsApp e
o Instagram mostrarem a imagem de preview quando o link é compartilhado.
Sem isso o link aparece "pelado", sem miniatura.

Se você usar domínio próprio depois, troque essas mesmas linhas pelo domínio
final.

---

## Domínio próprio

1. Compre o domínio (`serafine.com.br`, por exemplo).
2. No painel do registrador, aponte os registros A para os IPs do GitHub
   Pages e o CNAME de `www` para `SEU-USUARIO.github.io`. A lista atual de
   IPs está na documentação do GitHub Pages, que muda de tempos em tempos.
3. Em **Settings → Pages → Custom domain**, coloque o domínio e marque
   **Enforce HTTPS**.

---

## O que ainda falta no conteúdo

- **Fotos.** Todos os blocos com textura diagonal são espaços reservados.
  São necessárias: fachada, interior da loja, quatro fotos de categoria e
  quatro de produto. Enquanto não entrarem, o site funciona mas não vende.
- **Produtos.** Os quatro nomes de peça são exemplos, precisam vir do
  estoque real.
- **Depoimentos.** São avaliações reais do Google. Vale avisar as três
  pessoas que os textos estão no site.
- **Mapa.** Hoje é uma representação desenhada em CSS. Para o mapa real do
  Google, basta trocar a `<div class="mapa">` por um `<iframe>` de embed.

---

## Cores e fontes

| Uso | Valor |
| --- | --- |
| Ouro da marca | `#D0A459` |
| Grafite da marca | `#282828` |
| Azul das janelas coloniais | `#23486B` |
| Bege | `#EFE8D8` |
| Branco quente | `#FDFBF5` |

Títulos em Fraunces, textos em Archivo, etiquetas e medidas em DM Mono,
logotipo em Montserrat. Todas carregadas do Google Fonts.
