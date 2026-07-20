# Calculate Checkout Installments with Monetizze

Retrieves transparent checkout installment options from Monetizze.

## Endpoint

- **Method:** `POST`
- **Path:** `https://app.monetizze.com.br/checkout/transparente/parcelamento`
- **Base URL:** `https://api.monetizze.com.br/2.1`
- **Official documentation:** [Calculate Checkout Installments](https://api.monetizze.com.br/2.1/apidoc/#api-Checkout_Transparente-Parcelamento)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ctk` | body | `string` | yes | Checkout transparent CTK environment key. |
| `referencia` | body | `string` | yes | Product checkout reference used by Monetizze. |
| `valor` | body | `number` | yes | Order value used to calculate installments. |
| `maxParcelas` | body | `number` | yes | Maximum number of installments to calculate. |
