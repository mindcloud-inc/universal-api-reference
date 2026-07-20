# Filter Connections with Pabbly Hook

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/connections`
- **Base URL:** `https://hook.pabbly.com`
- **Official documentation:** [Filter Connections](https://apidocs.pabbly.com/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Connection status selector. |
| `folder_id` | query | `string` | yes | Folder ID selector. Pabbly returns Invalid folder ID when this endpoint is run without a valid folder_id. |
| `name` | query | `string` | no | Connection name selector. |
