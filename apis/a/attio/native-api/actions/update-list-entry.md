# Update List Entry with Attio

Updates a list entry in Attio.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/lists/:list/entries/:entry_id`
- **Base URL:** `https://api.attio.com`
- **Official documentation:** [Update List Entry](https://docs.attio.com/rest-api/endpoint-reference/entries/update-a-list-entry-overwrite)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list` | path | `string` | yes | The UUID or slug identifying the list. |
| `entry_id` | path | `string` | yes | The UUID identifying the list entry. |
| `entryValues` | body | `object` | yes | Entry values keyed by Attio attribute slug or attribute ID. This overwrite endpoint replaces current multiselect values. |
