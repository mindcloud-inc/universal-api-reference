# Reorder Tags with Habitica

Reorders tags in Habitica.

## Endpoint

- **Method:** `POST`
- **Path:** `/reorder-tags`
- **Base URL:** `https://habitica.com/api/v3`
- **Official documentation:** [Reorder Tags](https://habitica.com/apidoc/#api-Tag-ReorderTags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tagId` | body | `string` | yes | The Habitica tag ID to move. |
| `to` | body | `number` | yes | The zero-based position where the tag should be placed. |
