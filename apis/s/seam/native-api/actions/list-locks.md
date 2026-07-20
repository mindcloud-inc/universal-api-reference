# List Locks with Seam

Retrieves a list of locks from Seam.

## Endpoint

- **Method:** `POST`
- **Path:** `/locks/list`
- **Base URL:** `https://connect.getseam.com`
- **Official documentation:** [List Locks](https://docs.seam.co/latest/api/locks/list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `connected_account_id` | body | `string` | no | ID of the connected account for which you want to list locks. |
| `search` | body | `string` | no | Search string for locks. |
| `space_id` | body | `string` | no | ID of the space for which you want to list locks. |
