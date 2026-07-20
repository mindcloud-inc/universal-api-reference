# Generate Checkout Key with Monetizze

Retrieves a transparent checkout key from Monetizze.

## Endpoint

- **Method:** `GET`
- **Path:** `https://app.monetizze.com.br/checkout/transparente/js`
- **Base URL:** `https://api.monetizze.com.br/2.1`
- **Official documentation:** [Generate Checkout Key](https://api.monetizze.com.br/2.1/apidoc/#api-Checkout_Transparente-CTKEY)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ctk` | query | `string` | yes | Checkout transparent CTK environment key. |
| `referencia` | query | `string` | yes | Product checkout reference used by Monetizze. |
| `ip` | query | `string` | no | Optional buyer IP address. |
