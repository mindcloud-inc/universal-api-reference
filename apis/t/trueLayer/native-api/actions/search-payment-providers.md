# Search Payment Providers with TrueLayer

Searches payment providers in TrueLayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/payments-providers/search`
- **Base URL:** `https://api.truelayer-sandbox.com`
- **Official documentation:** [Search Payment Providers](https://docs.truelayer.com/reference/search-payment-providers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `countries[]` | body | `array<string>` | yes | ISO 3166-1 alpha-2 country codes to search payment providers for, such as GB. |
| `currencies[]` | body | `array<string>` | yes | ISO 4217 currency codes to search payment providers for, such as GBP. |
| `authorization_flow` | body | `object` | yes | Authorization flow filter. Example: {"configuration":{"redirect":{}}}. |
