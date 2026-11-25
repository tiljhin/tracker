# Tracker · TIL JHIN

Página pública da comunidade (GitHub Pages).

## Dar BIGOCOINS pelo Tracker (25/11/2026)
No card JARRO DO CASSINO, com `?admin` e senha, aparece a pastilha DAR BIGOCOINS. Ela abre uma telinha (@ do Bigodinho + quantidade) e chama a função `dar-moedas` do Supabase, que confere a senha do Tracker e usa o token do StreamElements guardado só como segredo da função (`SE_JWT`).
