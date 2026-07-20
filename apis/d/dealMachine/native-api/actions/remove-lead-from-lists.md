# Remove Lead From Lists with DealMachine

## Endpoint

- **Method:** `POST`
- **Path:** `/public/v1/leads/:lead_id/remove-from-list`
- **Base URL:** `https://api.dealmachine.com`
- **Official documentation:** [Remove Lead From Lists](https://docs.dealmachine.com/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lead_id` | path | `number` | yes | The DealMachine lead ID. |
| `list_ids` | body | `string` | yes | One or more DealMachine list IDs. Use a comma-separated string when sending multiple IDs. |
