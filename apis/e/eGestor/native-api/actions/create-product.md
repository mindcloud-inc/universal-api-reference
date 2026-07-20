# Create Product with eGestor

Creates a new product in eGestor.

## Endpoint

- **Method:** `POST`
- **Path:** `/produtos`
- **Base URL:** `https://api.egestor.com.br/api/v1`
- **Official documentation:** [Create Product](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L898)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `descricao` | body | `string` | yes | Descrição do produto. |
| `codigoProprio` | body | `string` | no | Código próprio do produto. |
| `estoque` | body | `number` | no | Quantidade em estoque. |
| `estoqueMinimo` | body | `number` | no | Estoque mínimo. |
| `controlarEstoque` | body | `boolean` | no | Define se o produto controla estoque. |
| `margemLucro` | body | `number` | no | Margem de lucro. |
| `precoCusto` | body | `number` | no | Preço de custo. |
| `precoVenda` | body | `number` | no | Preço de venda. |
| `origemFiscal` | body | `number` | no | Origem fiscal do produto. |
| `unidadeTributada` | body | `string` | no | Unidade tributada. |
| `codigoGrupoTributos` | body | `number` | no | Código do grupo de tributos vinculado. |
| `tags[]` | body | `array<string>` | no | Lista de tags do produto. |
