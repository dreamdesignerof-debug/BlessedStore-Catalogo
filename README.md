# Blessed Store — catálogo conectado ao Supabase

## Arquivos
- `index.html` e `app.js`: catálogo público e painel administrativo.
- `importar.html`: ferramenta de migração do catálogo HTML antigo para o Supabase Storage e tabela `products`.

## Configuração atual
- Supabase URL: `https://wdetfogymnbnbhaulhxv.supabase.co`
- Tabela: `public.products`
- Bucket: `catalogo` (público)
- Administrador esperado: `dreamdesignerof@gmail.com`
- O frontend usa somente a publishable key. Não inclua service_role/secret keys no repositório.

## Importar os produtos antigos
1. Publique primeiro este projeto em um preview/teste, não sobre o site principal.
2. Abra `importar.html` no preview, entre com a conta administradora e selecione o arquivo antigo `index (3).html`.
3. Clique em **Iniciar importação** e aguarde o resultado. A importação usa `legacy_id` como chave de upsert para evitar duplicatas.
4. Confira os produtos e imagens antes de trocar o domínio publicado.

## Publicação pelo GitHub
Depois de testar, conecte o repositório `dreamdesignerof-debug/BlessedStore-Catalogo` ao site Netlify existente, branch `main`, comando de build vazio e diretório de publicação `.`. Só então cada commit na branch principal deverá disparar um deploy automático.

## Segurança
- A autorização real do painel depende das políticas RLS do Supabase, não apenas da checagem de e-mail no JavaScript.
- Não coloque chaves `service_role` ou `secret` em arquivos públicos.
- Mantenha o site atual ativo até validar a migração e o novo deploy.
