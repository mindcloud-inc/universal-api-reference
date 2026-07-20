# Create Tag with TxtSync

Creates a new tag in TxtSync.

## Endpoint

- **Method:** `POST`
- **Path:** `/tags`
- **Base URL:** `https://api.txtsync.com`
- **Official documentation:** [Create Tag](https://docs.txtsync.com/#add-tag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Name` | body | `string` | yes | Unique tag name. |
| `ContactIDs` | body | `list<number>` | no | Optional contact IDs to subscribe to the new tag. Send multiple values as a array. |
