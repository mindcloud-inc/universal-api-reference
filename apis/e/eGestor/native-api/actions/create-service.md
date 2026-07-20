# Create Service with eGestor

Creates a new service in eGestor.

## Endpoint

- **Method:** `POST`
- **Path:** `/servicos`
- **Base URL:** `https://api.egestor.com.br/api/v1`
- **Official documentation:** [Create Service](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L1381)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `descricao` | body | `string` | yes | Descrição do serviço. |
| `precoVenda` | body | `number` | no | Preço de venda. |
| `codigoGrupoTributos` | body | `number` | no | Código do grupo de tributos vinculado. |
| `itemListaServico` | body | `string` | no | Código do item da lista de serviço. |
| `cnae` | body | `string` | no | Código CNAE. |
| `codTributacaoMun` | body | `string` | no | Código de tributação municipal. |
| `anotacoesInternas` | body | `string` | no | Anotações internas do serviço. |
| `tags[]` | body | `array<string>` | no | Lista de tags do serviço. |
