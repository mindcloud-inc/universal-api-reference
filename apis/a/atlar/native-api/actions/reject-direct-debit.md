# Reject direct debit with Atlar

Rejects a direct debit in Atlar.

## Endpoint

- **Method:** `POST`
- **Path:** `/payments/v2/direct-debits/{id}:reject`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [Reject direct debit](https://docs.atlar.com/reference/post-payments-v2-direct-debits-id-reject)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string<string>` | yes |
| `If-Match` | query | `string<string>` | no |
