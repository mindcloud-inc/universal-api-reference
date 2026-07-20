# Delete Multiple Sources with Chatsistant

Deletes multiple sources from Chatsistant.

## Endpoint

- **Method:** `POST`
- **Path:** `/data-sources/delete`
- **Base URL:** `https://app.chatsistant.com/api/v1`
- **Official documentation:** [Delete Multiple Sources](https://docs.chatsistant.com/api-reference/data-sources/delete_multi)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuids[]` | body | `array<string>` | yes | List of source UUIDs to delete. |
