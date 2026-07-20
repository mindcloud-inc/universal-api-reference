# List Users with Superchat

Retrieves users from a Superchat workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `https://api.superchat.com/v1.0`
- **Official documentation:** [List Users](https://developers.superchat.com/reference/listusers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `before` | query | `string` | no | Specify the cursor before which objects should be returned. |
