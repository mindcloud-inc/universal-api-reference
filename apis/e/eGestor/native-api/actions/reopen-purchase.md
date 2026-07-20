# Reopen Purchase with eGestor

Reopens a purchase in eGestor.

## Endpoint

- **Method:** `GET`
- **Path:** `/compras/:codigo/reabrir`
- **Base URL:** `https://api.egestor.com.br/api/v1`
- **Official documentation:** [Reopen Purchase](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L3445)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `codigo` | path | `number` | yes | Código da compra. |
