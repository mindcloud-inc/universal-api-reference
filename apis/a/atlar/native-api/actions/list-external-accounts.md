# List external accounts with Atlar

Retrieves external accounts from Atlar.

## Endpoint

- **Method:** `GET`
- **Path:** `/payments/v2/external-accounts`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [List external accounts](https://docs.atlar.com/reference/get-payments-v2-external-accounts)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `query` | query | `string<string>` | no |
| `counterpartyId` | query | `string<string>` | no |
| `entityIdsIn[]` | query | `array<string>` | no |
