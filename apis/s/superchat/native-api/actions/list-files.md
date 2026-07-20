# List Files with Superchat

Retrieves files from a Superchat workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/files`
- **Base URL:** `https://api.superchat.com/v1.0`
- **Official documentation:** [List Files](https://developers.superchat.com/reference/listfiles)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `before` | query | `string` | no | Specify the cursor before which objects should be returned. |
