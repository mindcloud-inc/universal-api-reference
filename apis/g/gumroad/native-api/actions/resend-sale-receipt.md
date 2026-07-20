# Resend Sale Receipt with Gumroad

Resends a sale receipt from Gumroad.

## Endpoint

- **Method:** `POST`
- **Path:** `/sales/:id/resend_receipt`
- **Base URL:** `https://api.gumroad.com/v2`
- **Official documentation:** [Resend Sale Receipt](https://gumroad.com/api#post-/sales/:id/resend_receipt)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The sale ID. |
