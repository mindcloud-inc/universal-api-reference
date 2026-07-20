# Reject direct debit batch with Atlar

Rejects a direct debit batch in Atlar.

## Endpoint

- **Method:** `POST`
- **Path:** `/payments/v2beta/direct-debit-batches/{id}:reject`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [Reject direct debit batch](https://docs.atlar.com/reference/post-payments-v2beta-direct-debit-batches-id-reject)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string<string>` | yes |
| `If-Match` | query | `string<string>` | no |
