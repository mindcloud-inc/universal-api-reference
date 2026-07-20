# List Receivables with eGestor

Retrieves a list of receivables from eGestor.

## Endpoint

- **Method:** `GET`
- **Path:** `/recebimentos`
- **Base URL:** `https://api.egestor.com.br/api/v1`
- **Official documentation:** [List Receivables](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L2457)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filtro` | query | `string` | no | Searches by receivable code, description, tags, or customer name. |
| `dtTipo` | query | `string` | no | Date field used by dtIni and dtFim. |
| `dtIni` | query | `string` | no | Start date in yyyy-mm-dd format. |
| `dtFim` | query | `string` | no | End date in yyyy-mm-dd format. |
| `caixa` | query | `number` | no | Internal cash account code. |
| `origem` | query | `string` | no | Receivable origin. |
| `conciliacao` | query | `string` | no | Bank reconciliation filter. |
| `planoContas` | query | `number` | no | Linked account plan code. |
| `obs` | query | `string` | no | Searches additional receivable notes. |
| `formaPgto` | query | `number` | no | Internal payment method code. |
| `numDoc` | query | `string` | no | Document number filter. |
| `situFin` | query | `number` | no | Receivable financial status code. |
| `boleto` | query | `string` | no | Filters receivables with or without boleto. |
| `recibo` | query | `string` | no | Filters receivables with or without receipt. |
| `fields` | query | `string` | no | Comma-separated response fields. |
| `orderBy` | query | `string` | no | Single sort definition in campo,direcao format. |
