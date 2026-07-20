# List direct debits with Atlar

Retrieves direct debits from Atlar.

## Endpoint

- **Method:** `GET`
- **Path:** `/payments/v2/direct-debits`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [List direct debits](https://docs.atlar.com/reference/get-payments-v2-direct-debits)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | query | `string<string>` | no |
| `status` | query | `string<string>` | no |
| `date` | query | `string<string>` | no |
| `scheme` | query | `string<string>` | no |
| `batchId` | query | `string<string>` | no |
