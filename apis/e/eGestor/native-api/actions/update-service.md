# Update Service with eGestor

Updates an existing service in eGestor.

## Endpoint

- **Method:** `PUT`
- **Path:** `/servicos/:codigo`
- **Base URL:** `https://api.egestor.com.br/api/v1`
- **Official documentation:** [Update Service](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L1474)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `codigo` | path | `number` | yes | Código do serviço. |
| `descricao` | body | `string` | yes | Descrição do serviço. |
| `precoVenda` | body | `number` | no | Preço de venda. |
| `codigoGrupoTributos` | body | `number` | no | Código do grupo de tributos vinculado. |
| `itemListaServico` | body | `string` | no | Código do item da lista de serviço. |
| `cnae` | body | `string` | no | Código CNAE. |
| `codTributacaoMun` | body | `string` | no | Código de tributação municipal. |
