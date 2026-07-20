# Update Boleto Due Date with Monetizze

Updates a boleto due date in Monetizze.

## Endpoint

- **Method:** `POST`
- **Path:** `/boleto`
- **Base URL:** `https://api.monetizze.com.br/2.1`
- **Official documentation:** [Update Boleto Due Date](https://api.monetizze.com.br/2.1/apidoc/#api-Produtor-Boleto)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transaction` | body | `number` | yes | Sale code whose boleto due date should be updated. |
| `data_vencimento` | body | `string` | yes | New boleto due date in yyyy-mm-dd format. |
