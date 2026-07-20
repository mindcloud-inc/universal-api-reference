# List Services with eGestor

Retrieves a list of services from eGestor.

## Endpoint

- **Method:** `GET`
- **Path:** `/servicos`
- **Base URL:** `https://api.egestor.com.br/api/v1`
- **Official documentation:** [List Services](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L1340)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filtro` | query | `string` | no | Busca a string informada nos campos código e descrição do serviço. |
| `fields` | query | `string` | no | Campos a retornar separados por vírgula. |
| `orderBy` | query | `string` | no | Ordenação da listagem no formato campo,direção. |
