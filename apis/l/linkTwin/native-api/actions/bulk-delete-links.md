# Bulk Delete Links with LinkTwin

Deletes multiple existing links from LinkTwin.

## Endpoint

- **Method:** `POST`
- **Path:** `/urls/delete`
- **Base URL:** `https://linktw.in/api`
- **Official documentation:** [Bulk Delete Links](https://linktw.in/developers#bulk-delete-links)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<number>` | yes | Link IDs to delete. |
