# List Entries with Attio

Retrieves list entries from Attio.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/lists/:list/entries/query`
- **Base URL:** `https://api.attio.com`
- **Official documentation:** [List Entries](https://docs.attio.com/rest-api/endpoint-reference/entries/query-list-entries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list` | path | `string` | yes | The UUID or slug identifying the list. |
| `filter` | body | `object` | no | Attio filter object for qualifying which entries to return. |
| `sorts[]` | body | `array<object>` | no | Attio sorts array for ordering list-entry results. |
| `limit` | body | `number` | no | Maximum number of list entries to return. |
| `offset` | body | `number` | no | Number of list entries to skip before returning results. |
