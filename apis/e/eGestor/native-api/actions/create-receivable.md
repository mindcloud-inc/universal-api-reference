# Create Receivable with eGestor

Creates a new receivable in eGestor.

## Endpoint

- **Method:** `POST`
- **Path:** `/recebimentos`
- **Base URL:** `https://api.egestor.com.br/api/v1`
- **Official documentation:** [Create Receivable](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L2536)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `codPlanoContas` | body | `number` | yes | Internal account plan code linked to the receivable. |
| `codFormaPgto` | body | `number` | no | Internal payment method code for the receivable. |
| `numDoc` | body | `string` | no | Document number for the receivable. |
| `descricao` | body | `string` | yes | Receivable description. |
| `valor` | body | `number` | yes | Receivable amount. |
| `dtVenc` | body | `string` | yes | Receivable due date in yyyy-mm-dd format. |
| `dtPgto` | body | `string` | no | Payment date in yyyy-mm-dd format. |
| `dtComp` | body | `string` | yes | Competence date in yyyy-mm-dd format. |
| `dtCred` | body | `string` | no | Credit date in yyyy-mm-dd format. |
| `recebido` | body | `boolean` | no | Whether the receivable is already received. |
| `codContato` | body | `number` | no | Internal contact code. |
| `codDisponivel` | body | `number` | yes | Internal cash account code. |
| `obs` | body | `string` | no | Additional receivable notes. |
| `tags` | body | `list<string>` | no | Tags to attach to the receivable. |
