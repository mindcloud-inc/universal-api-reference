# List Contact Lists with Superchat

Retrieves contact lists from a Superchat workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/contact-lists`
- **Base URL:** `https://api.superchat.com/v1.0`
- **Official documentation:** [List Contact Lists](https://developers.superchat.com/reference/listcontactlists)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `before` | query | `string` | no | Specify the cursor before which objects should be returned. |
