# List Opening Balances with Conta Azul

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/financeiro/eventos-financeiros/saldo-inicial`
- **Base URL:** `https://api-v2.contaazul.com`
- **Official documentation:** [List Opening Balances](https://developers.contaazul.com/open-api-docs/financial-apis-openapi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data_fim` | query | `date` | yes | Required upper date bound. |
| `data_inicio` | query | `date` | yes | Required lower date bound. |
