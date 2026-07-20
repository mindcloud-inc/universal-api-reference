# Create external account with Atlar

Creates an external account in Atlar.

## Endpoint

- **Method:** `POST`
- **Path:** `/payments/v2/external-accounts`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [Create external account](https://docs.atlar.com/reference/post-payments-v2-external-accounts)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `counterpartyId` | body | `string<string>` | yes |
| `market` | body | `string<string>` | yes |
| `identifiers[]` | body | `array<object>` | yes |
