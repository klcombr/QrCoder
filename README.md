# QrCoder

Gerador de QR codes a partir de URLs, com backend em Python/Flask e frontend em HTML, CSS e JavaScript puro. Não exige login ou cadastro: basta informar a URL para gerar e baixar o QR code como imagem PNG.

## Estrutura

```
backend/   API Flask com o endpoint POST /generate_qr (gera o QR code em PNG)
frontend/  Página estática (HTML, CSS, JS) que consome a API
```

## Funcionalidades

- Geração de QR code a partir de qualquer URL.
- Download do QR code gerado como imagem PNG.
- Interface responsiva, com animação de carregamento.
- CORS restrito à origem `https://km-qr.netlify.app`.

## Como rodar localmente

Instale as dependências do backend e inicie o servidor:

```bash
pip install -r backend/requirements.txt
python backend/app.py
```

Depois, abra o arquivo `frontend/index.html` no navegador, cole a URL e clique no botão para gerar o QR code. Para testar localmente com o frontend apontando para o backend local, ajuste a URL do `fetch` em `frontend/main.js` para `http://localhost:5000/generate_qr` (o CORS em produção permanece restrito a `https://km-qr.netlify.app`).

## Licença

MIT — veja [LICENSE](LICENSE).
