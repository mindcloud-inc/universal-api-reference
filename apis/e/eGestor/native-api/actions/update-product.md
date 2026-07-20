# Update Product with eGestor

Updates an existing product in eGestor.

## Endpoint

- **Method:** `PUT`
- **Path:** `/produtos/:codigo`
- **Base URL:** `https://api.egestor.com.br/api/v1`
- **Official documentation:** [Update Product](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L1019)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `codigo` | path | `number` | yes | Código do produto. |
| `descricao` | body | `string` | yes | Descrição do produto. |
| `codigoProprio` | body | `string` | no | Código próprio do produto. |
| `estoque` | body | `number` | no | Quantidade em estoque. |
| `controlarEstoque` | body | `boolean` | no | Define se o produto controla estoque. |
| `precoCusto` | body | `number` | no | Preço de custo. |
| `precoVenda` | body | `number` | no | Preço de venda. |
| `origemFiscal` | body | `number` | no | Origem fiscal do produto. |
| `unidadeTributada` | body | `string` | no | Unidade tributada. |
| `codigoGrupoTributos` | body | `number` | no | Código do grupo de tributos vinculado. |
