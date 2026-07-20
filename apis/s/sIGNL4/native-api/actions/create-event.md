# Create Event with SIGNL4

Creates an event in SIGNL4.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/events/{webhookIdOrTeamId}`
- **Base URL:** `https://connect.signl4.com/api`
- **Official documentation:** [Create Event](https://connect.signl4.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhookIdOrTeamId` | path | `string` | yes | Use team id to send an event straight to the team or an inbound webhook identifier (https://connect.signl4.com/webhook/{Identifier}) to use distribution rules |
| `ExtIdParam` | query | `string` | no | — |
| `ExtStatusParam` | query | `string` | no | — |
| `NewStatus` | query | `string` | no | — |
| `ResolvedStatus` | query | `string` | no | — |
| `AckStatus` | query | `string` | no | — |
