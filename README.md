# Portfólio profissional

Aplicação Django com página pública, painel de administração, perfil profissional, projetos, experiências e formulário privado de propostas.

## Implantação no Render

O código completo está em `portfolio_profissional_render.zip`. O comando de build extrai `portfolio_backend/`, instala as dependências e prepara os arquivos estáticos. Não há senhas nem banco de dados dentro do pacote.

O `render.yaml` define um serviço Python e PostgreSQL, ambos no plano gratuito e na região Virginia. Use o workspace **Portifólio**. A chave do Django é gerada pelo Render e a conexão do banco é vinculada pelo Blueprint.

O usuário administrador inicial é `admin`. A senha inicial é definida somente na variável `DJANGO_SUPERUSER_PASSWORD` do Render. Após o primeiro acesso, remova essa variável; a conta já criada é preservada.

O banco gratuito expira após 30 dias. Fotos e outros uploads locais não persistem entre reinícios: configure armazenamento externo antes de utilizar mídia em produção.

## Desenvolvimento

Extraia o ZIP e abra `portfolio_backend/`. O README interno descreve instalação, API, testes e configuração. Foram aprovados 25 testes locais com SQLite e a verificação de produção do Django. A implantação deve ser verificada no domínio público e no PostgreSQL após o deploy.
