# List Inboxes with Superchat

Retrieves inboxes from a Superchat workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/inboxes`
- **Base URL:** `https://api.superchat.com/v1.0`
- **Official documentation:** [List Inboxes](https://developers.superchat.com/reference/listinboxes)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `before` | query | `string` | no | Specify the cursor before which objects should be returned. |
