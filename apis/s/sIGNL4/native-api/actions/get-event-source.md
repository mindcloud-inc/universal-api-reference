# Get Event Source with SIGNL4

Retrieves an event source from SIGNL4 by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/eventsources/{eventSourceId}`
- **Base URL:** `https://connect.signl4.com/api`
- **Official documentation:** [Get Event Source](https://connect.signl4.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventSourceId` | path | `string` | yes | Id of the event source. |
| `language` | query | `number` | no | <p/><ul><li>0 = EN</li><li>1 = DE</li></ul> |
