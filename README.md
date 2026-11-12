# Semana 13 - Integração contínua

Dupla:

- Caio Jardim Muniz - RA 125794
- Kayke Sena Moraes - RA 112722

Testes de API com Postman, Newman e GitHub Actions.

## Testes

- Buscar o usuário 1: status 200.
- Buscar um usuário inexistente: status 404.
- Criar um post: status 201 e conferir os dados.

## Executar

Com Node.js instalado, execute:

```sh
npx --yes newman@6.2.1 run colecao.json --timeout-request 15000
```

## Pipeline

Os testes rodam a cada push. Confira o resultado na aba **Actions** do GitHub.

Para demonstrar uma falha, altere o ID esperado do usuário de `to.eql(1)` para `to.eql(2)` em `colecao.json` e envie. Depois restaure o valor e envie novamente.
