# List Channels with Superchat

Retrieves channels from a Superchat workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/channels`
- **Base URL:** `https://api.superchat.com/v1.0`
- **Official documentation:** [List Channels](https://developers.superchat.com/reference/listchannels)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `before` | query | `string` | no | Specify the cursor before which objects should be returned. |
