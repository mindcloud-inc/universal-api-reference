# Update Payment Request with GoAffPro

Updates an affiliate payment request in GoAffPro.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/admin/payments/requests/:id`
- **Base URL:** `https://api.goaffpro.com/v1`
- **Official documentation:** [Update Payment Request](https://api.goaffpro.com/docs/admin/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Payment request ID. |
| `status` | body | `string` | yes | New payment request status. |
