# List Products with eGestor

Retrieves a list of products from eGestor.

## Endpoint

- **Method:** `GET`
- **Path:** `/produtos`
- **Base URL:** `https://api.egestor.com.br/api/v1`
- **Official documentation:** [List Products](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L794)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filtro` | query | `string` | no | Busca a string informada nos campos código do produto, código próprio e nome do produto. |
| `controlarEstoque` | query | `list` | no | Filtra por produtos que controlam ou não controlam estoque. Valores documentados: 0 ou 1. Accepted values: `0`, `1`. |
| `fields` | query | `string` | no | Campos a retornar separados por vírgula. |
| `orderBy` | query | `string` | no | Ordenação da listagem no formato campo,direção. |
