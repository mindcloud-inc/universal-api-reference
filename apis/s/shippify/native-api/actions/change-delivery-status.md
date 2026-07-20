# Change Delivery Status with Shippify

Updates a delivery status in Shippify.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/deliveries/:id/status`
- **Base URL:** `https://api.shippify.co`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Shippify delivery identifier or reference ID whose status should change. |
| `status` | body | `string` | yes | New Shippify delivery status. |
| `comment` | body | `string` | yes | Comment explaining the delivery status change. |
| `author` | body | `object` | yes | Required object describing the operator or actor making the status change. |
| `reasonByCompany[]` | body | `array<object>` | no | Optional array of predefined company reasons for the status change. |
