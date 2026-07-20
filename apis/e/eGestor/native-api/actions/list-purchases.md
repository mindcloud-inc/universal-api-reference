# List Purchases with eGestor

Retrieves a list of purchases from eGestor.

## Endpoint

- **Method:** `GET`
- **Path:** `/compras`
- **Base URL:** `https://api.egestor.com.br/api/v1`
- **Official documentation:** [List Purchases](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L3111)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filtro` | query | `string` | no | Busca a string informada nos campos código da compra, palavras-chave e nome do fornecedor. |
