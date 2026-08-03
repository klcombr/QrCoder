# QrCoder

Gerador de QR codes a partir de URLs, com backend em Python/Flask e frontend em HTML, CSS e JavaScript. Não exige login ou cadastro: basta informar a URL para gerar e baixar o QR code como imagem PNG.

## Funcionalidades

- Geração de QR code a partir de qualquer URL.
- Download do QR code gerado como imagem PNG.
- Interface responsiva, com animação de carregamento.
- Endpoint `POST /generate_qr` no backend Flask.
- CORS configurado para o frontend hospedado.

## Como usar

Instale as dependências do backend e inicie o servidor:

```bash
pip install flask flask_cors qrcode[pil]
python backend/app.py
```

Depois, abra o arquivo `frontend/index.html` no navegador, cole a URL e clique no botão para gerar o QR code.

## Licença

MIT
