# Search Accounts Receivable with Conta Azul

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/financeiro/eventos-financeiros/contas-a-receber/buscar`
- **Base URL:** `https://api-v2.contaazul.com`
- **Official documentation:** [Search Accounts Receivable](https://developers.contaazul.com/open-api-docs/financial-apis-openapi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data_vencimento_ate` | query | `date` | yes | Required upper due-date bound. |
| `data_vencimento_de` | query | `date` | yes | Required lower due-date bound. |
| `pagina` | query | `number` | yes | Page number required by Conta Azul. |
| `tamanho_pagina` | query | `number` | yes | Page size required by Conta Azul. |
