# Search Transactions with Monetizze

Finds transactions in Monetizze by product, email, date, or status.

## Endpoint

- **Method:** `GET`
- **Path:** `/transactions`
- **Base URL:** `https://api.monetizze.com.br/2.1`
- **Official documentation:** [Search Transactions](https://api.monetizze.com.br/2.1/apidoc/#api-Geral-Transactions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product` | query | `number` | no | Filter by product code. |
| `transaction` | query | `number` | no | Filter by sale code. |
| `email` | query | `string` | no | Filter by buyer email. |
| `date_min` | query | `string` | no | Minimum transaction creation date and time in yyyy-mm-dd hh:mm:ss format. |
| `date_max` | query | `string` | no | Maximum transaction creation date and time in yyyy-mm-dd hh:mm:ss format. |
| `end_date_min` | query | `string` | no | Minimum finalized sale date and time in yyyy-mm-dd hh:mm:ss format. |
| `end_date_max` | query | `string` | no | Maximum finalized sale date and time in yyyy-mm-dd hh:mm:ss format. |
| `status` | query | `number` | no | Optional sale status filter values such as 1, 2, 3, 4, 5, or 6. Send multiple values as a array. |
| `forma_pagamento` | query | `number` | no | Optional payment method filter values such as 1, 3, 4, or 8. Send multiple values as a array. |
| `page` | query | `number` | no | Page number starting at 1. |
