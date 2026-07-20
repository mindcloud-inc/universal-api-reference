# Approve credit transfer with Atlar

Approves a credit transfer in Atlar.

## Endpoint

- **Method:** `POST`
- **Path:** `/payments/v2/credit-transfers/{id}:approve`
- **Base URL:** `https://api.atlar.com`
- **Official documentation:** [Approve credit transfer](https://docs.atlar.com/reference/post-payments-v2-credit-transfers-id-approve)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string<string>` | yes |
| `If-Match` | query | `string<string>` | no |
| `approvalStepId` | body | `string<string>` | yes |
