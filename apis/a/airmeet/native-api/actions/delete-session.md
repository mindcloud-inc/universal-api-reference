# Delete Session with Airmeet

Deletes an existing session from Airmeet.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/airmeet/{airmeetId}/session/{sessionId}`
- **Base URL:** `https://api-gateway-prod.us.airmeet.com/prod`
- **Official documentation:** [Delete Session](https://help.airmeet.com/support/solutions/articles/82000909770-3-manage-event-airmeet-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `airmeetId` | path | `string` | yes | The Airmeet event ID. |
| `sessionId` | path | `string` | yes | The session ID to delete. |
