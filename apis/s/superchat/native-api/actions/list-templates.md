# List Templates with Superchat

Retrieves templates from a Superchat workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/templates`
- **Base URL:** `https://api.superchat.com/v1.0`
- **Official documentation:** [List Templates](https://developers.superchat.com/reference/listtemplates)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `before` | query | `string` | no | Specify the cursor before which objects should be returned. |
| `channel_id` | query | `string` | no | — |
| `folder_id` | query | `string` | no | — |
