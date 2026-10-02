# Controle de Cartazes — versão mobile sem backend

Aplicação estática/PWA. Não usa Node, banco remoto ou API.

## Publicar rápido
Envie os arquivos desta pasta para qualquer hospedagem estática (Netlify, Cloudflare Pages, GitHub Pages etc.). O site precisa ser servido por HTTPS para a instalação PWA funcionar corretamente.

## Uso
1. Abra o site no celular.
2. Toque em **Atualizar base CSV** e selecione o arquivo exportado do ERP.
3. Vá em **Buscar**, procure pelo nome ou PRO_COD e toque em **Adicionar placa**.
4. Em **Placas**, copie os códigos ou exporte TXT/CSV.
5. Na próxima conferência, importe o CSV atualizado. O app compara preços com a base anterior.

## Dados
Os produtos e a lista ficam no IndexedDB do próprio navegador/dispositivo. Limpar os dados do site/navegador apaga a base local. Dados não sincronizam entre aparelhos.

## CSV esperado
Separador `;`, codificação Windows-1252/ANSI. Campos mínimos: PRO_COD, PRO_DESC e VENDA. Também reconhece DEP_COD, DEP_DESC, CAT_COD, CAT_DESC, QUANTIDADE, CUSTO e MARK_CALC.
