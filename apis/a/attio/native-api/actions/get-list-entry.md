# Get List Entry with Attio

Retrieves a list entry from Attio.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/lists/:list/entries/:entry_id`
- **Base URL:** `https://api.attio.com`
- **Official documentation:** [Get List Entry](https://docs.attio.com/rest-api/endpoint-reference/entries/get-a-list-entry)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list` | path | `string` | yes | The UUID or slug identifying the list. |
| `entry_id` | path | `string` | yes | The UUID identifying the list entry. |
