# Pay Payable with eGestor

Marks a payable as paid in eGestor.

## Endpoint

- **Method:** `PUT`
- **Path:** `/pagamentos/:codigo/pagar`
- **Base URL:** `https://api.egestor.com.br/api/v1`
- **Official documentation:** [Pay Payable](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L3049)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `codigo` | path | `number` | yes |
| `valor` | body | `number` | yes |
| `dtPgto` | body | `string` | yes |
| `dtComp` | body | `string` | yes |
