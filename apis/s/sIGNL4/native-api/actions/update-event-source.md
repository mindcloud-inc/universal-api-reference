# Update Event Source with SIGNL4

Updates an event source in SIGNL4.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/eventsources/{eventSourceId}`
- **Base URL:** `https://connect.signl4.com/api`
- **Official documentation:** [Update Event Source](https://connect.signl4.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventSourceId` | path | `string` | yes | ID of event source |
| `name` | body | `string` | no | — |
| `description` | body | `string` | no | — |
| `teamId` | body | `string` | no | — |
| `disabled` | body | `boolean` | no | — |
| `options` | body | `number` | no | <p/><ul><li>0 = None</li><li>1 = DisableContentParsing</li></ul> |
