# Terra Plena — Adubos & Insumos

Site institucional + loja online, em HTML/CSS/JS puro (sem framework, sem build).
Duas páginas: `index.html` (institucional) e `loja.html` (catálogo com carrinho e checkout por WhatsApp).

## Como colocar no GitHub (arrastar e soltar)

1. Em [github.com/new](https://github.com/new), crie um repositório vazio (ex.: `terraplena`) **sem** criar o README/`.gitignore` dele.
2. Abra a página do repositório novo e clique em **"uploading an existing file"** (ou *Add file → Upload files*).
3. **Arraste o CONTEÚDO desta pasta** (não a pasta, o que está dentro): `index.html`, `loja.html`, `README.md`, `LEIA-ME.txt`, `.nojekyll` e as pastas `assets/`, `logos/`, `products/`.
4. Clique em **Commit changes**.
5. Vá em **Settings → Pages** → *Deploy from a branch* → Branch: `main`, Folder: `/ (root)` → **Save**.
6. Em ~1 minuto o site está no ar em `https://SEU-USUARIO.github.io/terraplena/`.

### Domínio próprio (opcional)

1. Crie um arquivo chamado `CNAME` na raiz do repositório com uma única linha: o seu domínio (ex.: `www.terraplena.com.br`).
2. No seu registro de domínio, aponte 4 registros A para `185.199.108.153`, `185.199.109.153`, `185.199.110.153` e `185.199.111.153` (e/ou CNAME do subdomínio para o endereço `.github.io`).
3. O HTTPS é ativado automaticamente após alguns minutos.

### Alternativa por terminal

```
git init && git add -A && git commit -m "site v4"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/terraplena.git
git push -u origin main
```

## O que personalizar antes de publicar (procure-e-substitua)

| O quê | Onde |
|---|---|
| WhatsApp `5577999004398` | nos dois HTMLs (procure o número; aparece em vários botões) |
| Link da Google Play | constante `APP_PLAY` no `<script>` de cada página (coloque seu link entre as aspas) |
| CNPJ, e-mail e razão social | rodapé (busque `00.000.000/0001-00` e `sac@terraplena.com.br`) |
| Preços | bloco `const P = [...]` no início do `<script>` de cada página |
| Fotos de produto | pasta `products/` (mesmo nome de arquivo) |

## Avisos importantes

- **Preços** dos nossos produtos são de referência de mercado (cotação 08/11/2026). Revise antes de vender.
- Os **44 itens da linha parceira** (abas 🌱 Hortimax e 🚜 Plantio, Manejo e Colheita) mostram **"Sob consulta"** de propósito, como no catálogo de referência. Um deles ("Gráfite Agrícola SC 5kg") não tem foto no catálogo original e aparece com ícone da categoria.
- As **avaliações (4,9★ / 387 avaliações)** são ilustrativas — troque ou remova se quiser rigor total antes de publicar.
- O visual segue a estrutura do site de referência usado como molde (Araguaia), com textos, preços e marca próprios.

## Testar localmente

Abra `index.html` direto no navegador, ou:

```
python3 -m http.server 8000
```

e acesse `http://localhost:8000`.
