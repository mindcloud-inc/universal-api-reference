# Convert Currency with Mallabe

Retrieves a currency conversion from Mallabe.

## Endpoint

- **Method:** `POST`
- **Path:** `/currencies/convert`
- **Base URL:** `https://mallabe.p.rapidapi.com/v1`
- **Official documentation:** [Convert Currency](https://app.mallabe.com/currencies/convert/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | no | Source currency code. |
| `to` | body | `string` | yes | Target currency code. |
| `amount` | body | `number` | yes | Amount to convert. |
| `date` | body | `date` | no | Historical conversion date. |
| `webhookUrl` | body | `string` | no | Webhook URL for asynchronous callbacks. |
