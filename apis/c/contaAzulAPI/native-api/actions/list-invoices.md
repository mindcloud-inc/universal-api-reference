# List Invoices with Conta Azul

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/notas-fiscais`
- **Base URL:** `https://api-v2.contaazul.com`
- **Official documentation:** [List Invoices](https://developers.contaazul.com/open-api-docs/open-api-invoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data_final` | query | `date` | yes | Required final invoice date. |
| `data_inicial` | query | `date` | yes | Required initial invoice date. |
