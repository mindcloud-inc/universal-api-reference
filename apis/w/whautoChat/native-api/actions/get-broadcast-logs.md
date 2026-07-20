# Get Broadcast Logs with WhautoChat

Retrieves broadcast logs from WhautoChat.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/broadcasts/{broadcastId}/logs`
- **Base URL:** `https://api.whauto.chat`
- **Official documentation:** [Get Broadcast Logs](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/broadcast/#6-get-broadcast-logs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcastId` | path | `string` | yes | Broadcast unique ID |
