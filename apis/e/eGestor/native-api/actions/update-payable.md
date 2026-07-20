# Update Payable with eGestor

Updates an existing payable in eGestor.

## Endpoint

- **Method:** `PUT`
- **Path:** `/pagamentos/:codigo`
- **Base URL:** `https://api.egestor.com.br/api/v1`
- **Official documentation:** [Update Payable](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L3001)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `codigo` | path | `number` | yes |
| `codPlanoContas` | body | `number` | yes |
| `codFormaPgto` | body | `number` | no |
| `numDoc` | body | `string` | no |
| `descricao` | body | `string` | yes |
| `codDisponivel` | body | `number` | yes |
| `valor` | body | `number` | yes |
| `dtComp` | body | `string` | yes |
| `dtVenc` | body | `string` | yes |
| `codContato` | body | `number` | no |
| `obs` | body | `string` | no |
| `tags` | body | `list<string>` | no |
