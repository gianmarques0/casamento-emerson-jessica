# Emerson & Jessica — publicação

## Estado atual
- Configuração pública do Supabase preenchida em `config.js`.
- Banco com 50 presentes e imagens cadastrado.
- Reservas compartilhadas via função `reserve_gift`.
- **Não execute novamente** `banco_supabase.sql` em um banco com reservas: pode sobrescrever informações.

## Publicação no GitHub Pages
1. Crie um repositório público chamado `casamento-emerson-jessica` na sua conta do GitHub.
2. Envie todo o **conteúdo** desta pasta para a raiz do repositório (`index.html`, `config.js`, pasta `assets`).
3. Abra Settings > Pages > Build and deployment, selecione Deploy from a branch, `main`, `/(root)` e salve.
4. O endereço esperado, se o repositório tiver esse nome, será `https://gianmarques0.github.io/casamento-emerson-jessica/` — só fica válido após publicar.
5. Teste em dois dispositivos diferentes; escolha um presente de teste e confirme que ele ficou indisponível em ambos. Para desfazer uma reserva de teste, use Table Editor no Supabase e redefina `reserved=false`, `reserved_by=NULL`, `reserved_at=NULL`.

## Segurança
A chave `sb_publishable_...` é pública e pode ficar no navegador. Nunca coloque `service_role`, `sb_secret_...` ou sua senha no repositório. Os nomes de convidados são armazenados na coluna `reserved_by` e não retornam na consulta pública do site.

## Observação
O GitHub Pages exige repositório ou branch criado no GitHub. O sistema de reserva depende da disponibilidade do serviço Supabase.
