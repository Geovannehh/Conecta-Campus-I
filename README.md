# Conecta Campus · versão Ceuma

Plataforma Flask com identidade inspirada no azul, dourado e vermelho da Universidade Ceuma. Projeto acadêmico independente, sem vínculo oficial. Não há integração com os sistemas internos da instituição.

## Executar
No Windows deste computador, abra `iniciar.cmd`. Acesse http://127.0.0.1:5087. O iniciador reutiliza as dependências disponíveis no projeto original em Downloads. Em outro computador, instale Python e execute:

```sh
python -m venv .venv
.venv\Scripts\python -m pip install -r requirements.txt
.venv\Scripts\python -m flask --app flask_app run --port 5087
```

## O que mudou
- Navegação lateral, cabeçalho institucional e atalhos de serviços.
- Interface adaptável a celulares, foco de teclado e redução de movimento.
- Perfil e missões salvos no navegador; sem cadastro de aluno.
- Busca por perfil, categoria e texto sem acentos, com estado vazio correto.
- Avaliações e sugestões persistidas em SQLite; painel administrativo preservado.
- Indicação explícita de contatos e locais demonstrativos.

Para criar administrador, consulte `python manage_admin.py --help`. O banco é criado em `instance/` ao iniciar. Para hospedagem, configure SECRET_KEY, COOKIE_SECURE=1 e um servidor WSGI. O servidor local é destinado ao desenvolvimento.

## Verificação
Páginas inicial, saúde, login e proteção do painel verificadas com cliente Flask. Sugestão, avaliação e interação retornam 201; nota inválida retorna 400. Sintaxe JavaScript validada. Interface e busca verificadas no navegador.

Referência visual: https://www.extranet.ceuma.br/novoportal/
