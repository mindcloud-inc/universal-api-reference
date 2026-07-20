# Get Receivable with eGestor

Retrieves details for a receivable from eGestor.

## Endpoint

- **Method:** `GET`
- **Path:** `/recebimentos/:codigo`
- **Base URL:** `https://api.egestor.com.br/api/v1`
- **Official documentation:** [Get Receivable](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L2582)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `codigo` | path | `number` | yes | Internal receivable code. |
