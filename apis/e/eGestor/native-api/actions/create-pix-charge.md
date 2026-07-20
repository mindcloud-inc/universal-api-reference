# Create Pix Charge with eGestor

Creates a new Pix charge in eGestor.

## Endpoint

- **Method:** `POST`
- **Path:** `/pix`
- **Base URL:** `https://api.egestor.com.br/api/v1`
- **Official documentation:** [Create Pix Charge](https://github.com/eGestor/documentacao-api/blob/master/apiary.apib#L4792)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `codFinanceiro` | body | `number` | yes | Código do financeiro para gerar a cobrança Pix. |
