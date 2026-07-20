# Reject credit transfer batch with Atlar

Rejects a credit transfer batch in Atlar.

## Endpoint

- **Method:** `POST`
- **Path:** `/payments/v2/credit-transfer-batches/{id}:reject`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [Reject credit transfer batch](https://docs.atlar.com/reference/post-payments-v2-credit-transfer-batches-id-reject)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string<string>` | yes |
| `If-Match` | query | `string<string>` | no |
