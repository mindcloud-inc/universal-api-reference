# List Conversations with Superchat

Retrieves conversations from a Superchat workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/conversations`
- **Base URL:** `https://api.superchat.com/v1.0`
- **Official documentation:** [List Conversations](https://developers.superchat.com/reference/listconversations)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `before` | query | `string` | no | Specify the cursor before which objects should be returned. |
