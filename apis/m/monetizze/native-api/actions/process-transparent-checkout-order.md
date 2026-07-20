# Process Transparent Checkout Order with Monetizze

Creates a transparent checkout order in Monetizze.

## Endpoint

- **Method:** `POST`
- **Path:** `https://app.monetizze.com.br/checkout/transparente/processar`
- **Base URL:** `https://api.monetizze.com.br/2.1`
- **Official documentation:** [Process Transparent Checkout Order](https://api.monetizze.com.br/2.1/apidoc/#api-Checkout_Transparente-Tracking)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payload` | body | `object` | yes | Full Monetizze transparent checkout processing JSON object as documented for this endpoint. |
