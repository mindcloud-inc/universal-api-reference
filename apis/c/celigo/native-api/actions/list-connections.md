# List Connections with Celigo

## Endpoint

- **Method:** `GET`
- **Path:** `/connections`
- **Base URL:** `https://{apiHost}/v1`
- **Official documentation:** [List Connections](https://developer.celigo.com/api/api-reference/connections-and-http-connectors/connections)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `externalId` | query | `string` | no | Only return connections with this exact external identifier. |
| `fetchQueueSize` | query | `boolean` | no | Include queue size information for each connection. |
