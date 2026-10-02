# Controle de Cartazes Mobile v2

Sistema 100% front-end para conferência de placas no celular.

## O que mudou
- Importa o CSV com a coluna `GTIN`.
- Agrupa automaticamente linhas repetidas pelo `PRO_COD`: 1 produto pode ter vários GTINs.
- Busca por nome, código interno ou GTIN.
- Scanner pela câmera compatível com iPhone/Safari e Android usando html5-qrcode (requer HTTPS e permissão de câmera).
- Se um GTIN estiver associado a mais de um produto, mostra as opções em vez de escolher automaticamente.
- IndexedDB: base e lista de placas ficam salvas no aparelho.
- Comparação de preços entre importações.
- Exportação TXT/CSV e cópia dos códigos internos.
- PWA instalável.

## Publicar
Envie todos os arquivos desta pasta para uma hospedagem estática HTTPS (Netlify, Cloudflare Pages, GitHub Pages etc.). Não precisa de Node, banco ou backend.

## Uso
1. Abra o site no celular.
2. Importe o CSV atualizado do ERP.
3. Toque em Escanear e permita a câmera.
4. Leia o código de barras e toque em Adicionar placa.
5. No fim, abra Placas e copie/exporte os códigos.

Observação: câmera via navegador exige HTTPS (localhost também é aceito em desenvolvimento). Caso o navegador não ofereça BarcodeDetector, use a busca manual por GTIN/nome/código.
