# Update Sale with eGestor

Updates an existing sale in eGestor.

## Endpoint

- **Method:** `PUT`
- **Path:** `/vendas/:codigo`
- **Base URL:** `https://api.egestor.com.br/api/v1`
- **Official documentation:** [Update Sale](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L3863)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `codigo` | path | `number` | yes | Código da venda. |
| `situacao` | body | `list` | yes | Nova situação da venda. Accepted values: `10`, `50`. |
| `situacaoOS` | body | `string` | no | Nova situação da ordem de serviço. |
| `campoAdicional1` | body | `string` | no | Conteúdo do campo adicional 1. |
| `campoAdicional2` | body | `string` | no | Conteúdo do campo adicional 2. |
| `campoAdicional3` | body | `string` | no | Conteúdo do campo adicional 3. |
| `campoAdicional4` | body | `string` | no | Conteúdo do campo adicional 4. |
