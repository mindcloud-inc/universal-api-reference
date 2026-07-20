# Approve direct debit with Atlar

Approves a direct debit in Atlar.

## Endpoint

- **Method:** `POST`
- **Path:** `/payments/v2/direct-debits/{id}:approve`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [Approve direct debit](https://docs.atlar.com/reference/post-payments-v2-direct-debits-id-approve)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string<string>` | yes |
| `If-Match` | query | `string<string>` | no |
| `approvalStepId` | body | `string<string>` | yes |
