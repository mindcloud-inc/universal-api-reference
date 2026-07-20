# Create Payable with eGestor

Creates a new payable in eGestor.

## Endpoint

- **Method:** `POST`
- **Path:** `/pagamentos`
- **Base URL:** `https://api.egestor.com.br/api/v1`
- **Official documentation:** [Create Payable](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L2838)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `codPlanoContas` | body | `number` | yes |
| `codFormaPgto` | body | `number` | no |
| `numDoc` | body | `string` | no |
| `descricao` | body | `string` | yes |
| `valor` | body | `number` | yes |
| `dtVenc` | body | `string` | yes |
| `dtComp` | body | `string` | yes |
| `dtPgto` | body | `string` | no |
| `pago` | body | `boolean` | no |
| `codContato` | body | `number` | no |
| `codDisponivel` | body | `number` | yes |
| `obs` | body | `string` | no |
| `tags` | body | `list<string>` | no |
