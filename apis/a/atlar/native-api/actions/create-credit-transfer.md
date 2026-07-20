# Create credit transfer with Atlar

Creates a credit transfer in Atlar.

## Endpoint

- **Method:** `POST`
- **Path:** `/payments/v2/credit-transfers`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [Create credit transfer](https://docs.atlar.com/reference/post-payments-v2-credit-transfers)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `amount` | body | `string<string>` | yes |
| `scheme` | body | `string<string>` | yes |
| `date` | body | `date<string>` | yes |
| `source` | body | `object<string>` | yes |
| `destination` | body | `string<string>` | yes |
| `reference` | body | `string<string>` | yes |
