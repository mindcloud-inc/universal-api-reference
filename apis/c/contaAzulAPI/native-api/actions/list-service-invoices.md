# List Service Invoices with Conta Azul

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/notas-fiscais-servico`
- **Base URL:** `https://api-v2.contaazul.com`
- **Official documentation:** [List Service Invoices](https://developers.contaazul.com/open-api-docs/open-api-invoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data_competencia_ate` | query | `date` | yes | Required competence end date. |
| `data_competencia_de` | query | `date` | yes | Required competence start date. |
