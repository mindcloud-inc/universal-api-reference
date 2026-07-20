# Create Sale Refund with Kiwify

Creates a sale refund in Kiwify.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/sales/:id/refund`
- **Base URL:** `https://public-api.kiwify.com`
- **Official documentation:** [Create Sale Refund](https://docs.kiwify.com.br/api-reference/sales/refund)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `pixKey` | body | `string` | no |
