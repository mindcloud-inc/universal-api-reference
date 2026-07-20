# List Contact Tags with TxtSync

Retrieves tags associated with a contact in TxtSync.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/:id/tags`
- **Base URL:** `https://api.txtsync.com`
- **Official documentation:** [List Contact Tags](https://docs.txtsync.com/#get-associated-tags)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Contact identifier. |
