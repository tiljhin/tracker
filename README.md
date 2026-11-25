# Tracker · TIL JHIN

Página pública da comunidade (GitHub Pages: `tiljhin.github.io/tracker`). Mostra a fila da live, BigoFlix, cassino, roleta, jogo da capa e rankings; lê o Supabase. A documentação completa fica na pasta local "TRACKER · Página pública".

## Área admin (`?admin` + senha)
Caixa **CASSINO**, abaixo do BIGOFLIX (25/11/2026):
- **DAR BIGOCOINS:** @ do Bigodinho + quantidade (negativo tira; limite 100.000 por vez), com VER SALDO e confirmação. Chama a função `dar-moedas` do Supabase, que confere a senha do Tracker e usa o token do StreamElements guardado só como segredo da função (`SE_JWT`).
- **MOEDAS EXTRAS NO JARRO:** soma um valor ao jarro do cassino (rodada especial; o jarro continua começando em 500). Grava em `cassino_extra` (função `cassino_extra_add`); o widget do Cassino pega a cada 4 s e enche o jarro. O extra fica **fora do % do pote**: o widget manda `extra` junto do jarro e o Tracker desconta (`jvPct`).

Sem senha no código; só a chave pública do Supabase aparece.
