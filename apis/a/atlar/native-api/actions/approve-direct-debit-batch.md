# Approve direct debit batch with Atlar

Approves a direct debit batch in Atlar.

## Endpoint

- **Method:** `POST`
- **Path:** `/payments/v2beta/direct-debit-batches/{id}:approve`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [Approve direct debit batch](https://docs.atlar.com/reference/post-payments-v2beta-direct-debit-batches-id-approve)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string<string>` | yes |
| `If-Match` | query | `string<string>` | no |
| `approvalStepId` | body | `string<string>` | yes |
