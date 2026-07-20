# Check Pix Status with eGestor

Retrieves the status of a Pix charge from eGestor.

## Endpoint

- **Method:** `GET`
- **Path:** `/pix/:codigo/consultarSituacao`
- **Base URL:** `https://api.egestor.com.br/api/v1`
- **Official documentation:** [Check Pix Status](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L4941)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `codigo` | path | `number` | yes | Código do Pix. |
