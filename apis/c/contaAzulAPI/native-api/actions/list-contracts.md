# List Contracts with Conta Azul

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/contratos`
- **Base URL:** `https://api-v2.contaazul.com`
- **Official documentation:** [List Contracts](https://developers.contaazul.com/open-api-docs/contracts-apis-openapi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data_fim` | query | `date` | yes | Required upper date bound. |
| `data_inicio` | query | `date` | yes | Required lower date bound. |
