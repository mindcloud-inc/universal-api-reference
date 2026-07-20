# Create Session with Airmeet

Creates a new session in Airmeet.

## Endpoint

- **Method:** `POST`
- **Path:** `/airmeet/{airmeetId}/session`
- **Base URL:** `https://api-gateway-prod.us.airmeet.com/prod`
- **Official documentation:** [Create Session](https://help.airmeet.com/support/solutions/articles/82000909770-3-manage-event-airmeet-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `airmeetId` | path | `string` | yes | The Airmeet event ID. |
| `hostEmail` | body | `string` | yes | Email of the host or community team member running the session. |
| `sessionDuration` | body | `number` | yes | Session duration in minutes. |
| `sessionStartTime` | body | `number` | yes | Session start time as a Unix timestamp in milliseconds. |
| `sessionTitle` | body | `string` | yes | Title of the session. |
