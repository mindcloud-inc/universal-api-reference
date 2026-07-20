# Get Event with SIGNL4

Retrieves an event from SIGNL4 by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/events/{eventId}`
- **Base URL:** `https://connect.signl4.com/api`
- **Official documentation:** [Get Event](https://connect.signl4.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | Event id for the event you want to get |
| `language` | query | `number` | no | <p/><ul><li>0 = EN</li><li>1 = DE</li></ul> |
