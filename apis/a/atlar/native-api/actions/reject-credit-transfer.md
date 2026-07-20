# Reject credit transfer with Atlar

Rejects a credit transfer in Atlar.

## Endpoint

- **Method:** `POST`
- **Path:** `/payments/v2/credit-transfers/{id}:reject`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [Reject credit transfer](https://docs.atlar.com/reference/post-payments-v2-credit-transfers-id-reject)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string<string>` | yes |
| `If-Match` | query | `string<string>` | no |
