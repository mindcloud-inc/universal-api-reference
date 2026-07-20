# Update Deal with Nimble

Updates an existing deal in Nimble.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v2/deals/:deal_id`
- **Base URL:** `https://app.nimble.com`
- **Official documentation:** [Update Deal](https://www.nimble.com/developers/docs/#tag/Deals/operation/put-deal)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deal_id` | path | `string` | yes | Nimble deal_id path parameter. |
| `tags[]` | body | `array<string>` | no | — |
| `fields_values` | body | `object` | no | — |
| `pipeline_id` | body | `string` | no | — |
| `stage_id` | body | `string` | no | — |
