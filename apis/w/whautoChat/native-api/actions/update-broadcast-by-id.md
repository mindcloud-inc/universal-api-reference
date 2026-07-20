# Update Broadcast by ID with WhautoChat

Updates an existing broadcast in WhautoChat by ID.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/broadcasts/{broadcastId}`
- **Base URL:** `https://api.whauto.chat`
- **Official documentation:** [Update Broadcast by ID](https://help.whauto.chat/cloud-version/integrations/rest-api/endpoints/broadcast/#4-update-broadcast-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `broadcastId` | path | `string` | yes | Broadcast unique ID |
| `workspace.id` | body | `string` | no | — |
| `name` | body | `string` | no | — |
| `type` | body | `string` | no | — |
