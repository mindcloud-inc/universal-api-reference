# List Pix Charges with eGestor

Retrieves a list of Pix charges from eGestor.

## Endpoint

- **Method:** `GET`
- **Path:** `/pix`
- **Base URL:** `https://api.egestor.com.br/api/v1`
- **Official documentation:** [List Pix Charges](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L4744)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filtro` | query | `string` | no | Busca por código do Pix ou nome do cliente. |
| `orderBy` | query | `string` | no | Campo e direção de ordenação, separados por vírgula. |
