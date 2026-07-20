# Create Voice Campaign with Go4Clients

Creates a new voice campaign in Go4Clients.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/campaigns/voice/v1.0`
- **Base URL:** `https://cloud.go4clients.com:8580`
- **Official documentation:** [Create Voice Campaign](https://apidoc.go4clients.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Campaign name to identify the call in analytics. |
| `sender` | body | `string` | yes | Caller ID shown to recipients. |
| `description` | body | `string` | no | Optional voice campaign description. |
| `callAttempts` | body | `string` | no | Number of call attempts per destination. |
| `timeBetweenDials` | body | `number` | no | Minutes between call attempts. |
| `currentCalls` | body | `number` | no | Maximum simultaneous calls. |
| `earliestTimeToCall` | body | `string` | no | Earliest allowed local time in HH:mm format. |
| `latestTimeToCall` | body | `string` | no | Latest allowed local time in HH:mm format. |
| `nextDayContinuation` | body | `boolean` | no | Continue the campaign on the next day when the call window ends. |
