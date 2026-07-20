# Update Receivable with eGestor

Updates an existing receivable in eGestor.

## Endpoint

- **Method:** `PUT`
- **Path:** `/recebimentos/:codigo`
- **Base URL:** `https://api.egestor.com.br/api/v1`
- **Official documentation:** [Update Receivable](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L2662)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `codigo` | path | `number` | yes |
| `codPlanoContas` | body | `number` | yes |
| `codFormaPgto` | body | `number` | no |
| `numDoc` | body | `string` | no |
| `descricao` | body | `string` | yes |
| `valor` | body | `number` | yes |
| `dtVenc` | body | `string` | yes |
| `dtComp` | body | `string` | yes |
| `dtCred` | body | `string` | no |
| `codContato` | body | `number` | no |
| `codDisponivel` | body | `number` | yes |
| `obs` | body | `string` | no |
| `tags` | body | `list<string>` | no |
