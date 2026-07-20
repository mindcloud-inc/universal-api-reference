# Delete Custom Sources by IDs with Chat Aid

Deletes custom sources from Chat Aid by IDs or filters.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/external/sources/custom`
- **Base URL:** `https://api.chataid.com`
- **Official documentation:** [Delete Custom Sources by IDs](https://docs.chataid.com/api-guide/custom-sources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<string>` | yes | Array of custom source IDs to delete. |
