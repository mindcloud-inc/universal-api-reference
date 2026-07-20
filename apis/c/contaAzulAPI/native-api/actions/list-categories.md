# List Categories with Conta Azul

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/categorias`
- **Base URL:** `https://api-v2.contaazul.com`
- **Official documentation:** [List Categories](https://developers.contaazul.com/open-api-docs/financial-apis-openapi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pagina` | query | `number` | yes | Page number required by Conta Azul. |
| `permite_apenas_filhos` | query | `boolean` | yes | Required Conta Azul category filter. |
| `tamanho_pagina` | query | `number` | yes | Page size required by Conta Azul. |
