# Create Deal with Nimble

Creates a new deal in Nimble.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/deals`
- **Base URL:** `https://app.nimble.com`
- **Official documentation:** [Create Deal](https://www.nimble.com/developers/docs/#tag/Deals/operation/create-new-deal)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `pipeline_id` | body | `string` | yes |
| `stage_id` | body | `string` | yes |
| `fields_values` | body | `object` | yes |
| `tags[]` | body | `array<string>` | no |
