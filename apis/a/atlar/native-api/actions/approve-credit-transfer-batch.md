# Approve credit transfer batch with Atlar

Approves a credit transfer batch in Atlar.

## Endpoint

- **Method:** `POST`
- **Path:** `/payments/v2/credit-transfer-batches/{id}:approve`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [Approve credit transfer batch](https://docs.atlar.com/reference/post-payments-v2-credit-transfer-batches-id-approve)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string<string>` | yes |
| `If-Match` | query | `string<string>` | no |
| `approvalStepId` | body | `string<string>` | yes |
