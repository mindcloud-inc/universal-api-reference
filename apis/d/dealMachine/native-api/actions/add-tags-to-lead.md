# Add Tags To Lead with DealMachine

## Endpoint

- **Method:** `POST`
- **Path:** `/public/v1/leads/:lead_id/add-tags`
- **Base URL:** `https://api.dealmachine.com`
- **Official documentation:** [Add Tags To Lead](https://docs.dealmachine.com/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lead_id` | path | `number` | yes | The DealMachine lead ID. |
| `tag_ids` | body | `string` | yes | One or more DealMachine tag IDs. Use a comma-separated string when sending multiple IDs. |
