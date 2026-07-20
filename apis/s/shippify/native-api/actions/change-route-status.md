# Change Route Status with Shippify

Updates a route status in Shippify.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/routes/:id/status`
- **Base URL:** `https://api.shippify.co`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Identifier of the route whose status should change. |
| `status` | body | `string` | yes | New Shippify route status. |
| `comment` | body | `string` | yes | Comment explaining the route status change. |
| `author` | body | `object` | yes | Required object describing the operator or actor making the route status change. |
| `reasonByCompany[]` | body | `array<object>` | no | Optional array of predefined company reasons for the route status change. |
