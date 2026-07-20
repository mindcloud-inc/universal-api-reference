# Update Entry with Zenkit

Updates an existing item in Zenkit.

## Endpoint

- **Method:** `PUT`
- **Path:** `/lists/:listId/entries/:listEntryId`
- **Base URL:** `https://zenkit.com/api/v1`
- **Official documentation:** [Update Entry](https://app.zenkit.com/docs/api/entries/put-api-v1-lists-listid-entries-listentryid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `listEntryId` | path | `string` | yes | The list entry id |
| `listId` | path | `string` | yes | The list id |
