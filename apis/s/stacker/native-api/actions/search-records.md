# Search Records with Stacker

Finds records in a Stacker object.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/external/objects/:object_sid/search/`
- **Base URL:** `https://api.go.stackerhq.com`
- **Official documentation:** [Search Records](https://docs.stackerhq.com/stacker/ai-and-automations/open-api-overview/record-actions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | body | `number` | no | Maximum number of records to return. |
| `filters[]` | body | `array<object>` | no | Array of filter conditions for the record search. |
| `include_fields[]` | body | `array<string>` | no | Field API names to include in the response. |
| `object_sid` | path | `string` | yes | Object SID from the Stacker endpoint path. |
| `order_by` | body | `string` | no | Field API name to sort by. Prefix with '-' for descending order. |
| `search` | body | `string` | no | Text to search across the selected fields. |
| `search_fields[]` | body | `array<string>` | no | Field API names to search across. |
| `start` | body | `number` | no | Zero-based starting index for the returned records. |
| `X-Account-Id` | body | `string` | yes | Stacker account ID sent as the X-Account-Id header. |
| `X-Stack-Id` | body | `string` | yes | Stacker stack ID sent as the X-Stack-Id header. |
