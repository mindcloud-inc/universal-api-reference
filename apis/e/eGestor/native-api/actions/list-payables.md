# List Payables with eGestor

Retrieves a list of payables from eGestor.

## Endpoint

- **Method:** `GET`
- **Path:** `/pagamentos`
- **Base URL:** `https://api.egestor.com.br/api/v1`
- **Official documentation:** [List Payables](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L2767)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `filtro` | query | `string` | no |
| `dtTipo` | query | `string` | no |
| `dtIni` | query | `string` | no |
| `dtFim` | query | `string` | no |
| `caixa` | query | `number` | no |
| `origem` | query | `string` | no |
| `conciliacao` | query | `string` | no |
| `planoContas` | query | `number` | no |
| `obs` | query | `string` | no |
| `formaPgto` | query | `number` | no |
| `numDoc` | query | `string` | no |
| `situFin` | query | `number` | no |
| `boleto` | query | `string` | no |
| `recibo` | query | `string` | no |
| `fields` | query | `string` | no |
| `orderBy` | query | `string` | no |
