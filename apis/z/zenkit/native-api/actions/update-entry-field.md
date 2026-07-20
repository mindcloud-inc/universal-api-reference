# Update Entry Field with Zenkit

Updates a field on an existing Zenkit item.

## Endpoint

- **Method:** `PUT`
- **Path:** `/lists/:listId/entries/:listEntryId/elements/:elementId`
- **Base URL:** `https://zenkit.com/api/v1`
- **Official documentation:** [Update Entry Field](https://app.zenkit.com/docs/api/entries/put-api-v1-lists-listid-entries-listentryid-elements-elementid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `elementId` | path | `string` | yes | The element id |
| `listEntryId` | path | `string` | yes | The list entry id |
| `listId` | path | `string` | yes | The list id |
