# List Acquittances By Installment with Conta Azul

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/financeiro/eventos-financeiros/parcelas/{parcela_id}/baixa`
- **Base URL:** `https://api-v2.contaazul.com`
- **Official documentation:** [List Acquittances By Installment](https://developers.contaazul.com/open-api-docs/acquittance-apis-openapi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parcela_id` | path | `string` | yes | Conta Azul installment identifier from the path. |
