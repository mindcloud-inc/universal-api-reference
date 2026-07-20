# List mandates with Atlar

Retrieves mandates from Atlar.

## Endpoint

- **Method:** `GET`
- **Path:** `/payments/v2/mandates`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [List mandates](https://docs.atlar.com/reference/get-payments-v2-mandates)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `externalAccountId` | query | `string<string>` | no |
| `counterpartyId` | query | `string<string>` | no |
| `status` | query | `string<string>` | no |
| `scheme` | query | `string<string>` | no |
