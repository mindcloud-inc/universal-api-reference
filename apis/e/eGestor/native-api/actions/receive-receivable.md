# Receive Receivable with eGestor

Marks a receivable as received in eGestor.

## Endpoint

- **Method:** `PUT`
- **Path:** `/recebimentos/:codigo/receber`
- **Base URL:** `https://api.egestor.com.br/api/v1`
- **Official documentation:** [Receive Receivable](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L2708)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `codigo` | path | `number` | yes |
| `valor` | body | `number` | yes |
| `dtPgto` | body | `string` | yes |
| `dtComp` | body | `string` | yes |
