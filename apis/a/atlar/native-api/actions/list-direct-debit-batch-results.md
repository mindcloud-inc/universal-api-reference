# List direct debit batch results with Atlar

Retrieves direct debit batch results from Atlar.

## Endpoint

- **Method:** `GET`
- **Path:** `/payments/v2beta/direct-debit-batches/{id}/results`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [List direct debit batch results](https://docs.atlar.com/reference/get-payments-v2beta-direct-debit-batches-id-results)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string<string>` | yes |
| `errors` | query | `boolean<string>` | no |
| `skipped` | query | `boolean<string>` | no |
