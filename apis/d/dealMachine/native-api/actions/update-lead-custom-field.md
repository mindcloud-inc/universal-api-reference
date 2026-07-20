# Update Lead Custom Field with DealMachine

## Endpoint

- **Method:** `POST`
- **Path:** `/public/v1/leads/:lead_id/custom-field`
- **Base URL:** `https://api.dealmachine.com`
- **Official documentation:** [Update Lead Custom Field](https://docs.dealmachine.com/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lead_id` | path | `number` | yes | The DealMachine lead ID. |
| `custom_field_id` | body | `number` | yes | The DealMachine custom field ID to update. |
| `value` | body | `string` | yes | The value to write into the custom field. |
