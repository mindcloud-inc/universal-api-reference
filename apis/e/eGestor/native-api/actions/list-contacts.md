# List Contacts with eGestor

Retrieves a list of contacts from eGestor.

## Endpoint

- **Method:** `GET`
- **Path:** `/contatos`
- **Base URL:** `https://api.egestor.com.br/api/v1`
- **Official documentation:** [List Contacts](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L201)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filtro` | query | `string` | no | Busca a string informada nos campos nome, fantasia, código, contato, email, telefone e tags. |
| `endereco` | query | `string` | no | Busca a string informada no endereço do contato. |
| `telefone` | query | `string` | no | Busca o valor informado no campo telefones do contato. |
| `email` | query | `string` | no | Busca o valor informado no campo e-mails do contato. |
| `clienteFinal` | query | `list` | no | Filtra por cliente final. Valores documentados: 1 sim, 2 não. Accepted values: `1`, `2`. |
| `indIE` | query | `list` | no | Filtra por indicador de IE. Valores documentados: 1 contribuinte, 2 isento, 9 não contribuinte. Accepted values: `1`, `2`, `9`. |
| `IE` | query | `string` | no | Filtra por inscrição estadual. |
| `IM` | query | `string` | no | Filtra por inscrição municipal. |
| `suframa` | query | `string` | no | Filtra pelo código SUFRAMA. |
| `obs` | query | `string` | no | Busca a string informada nas observações do contato. |
| `fields` | query | `string` | no | Campos a retornar separados por vírgula. |
| `orderBy` | query | `string` | no | Ordenação da listagem no formato campo,direção. |
