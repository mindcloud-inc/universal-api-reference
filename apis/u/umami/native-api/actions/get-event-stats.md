# Get Event Stats with Umami

## Endpoint

- **Method:** `GET`
- **Path:** `/websites/:websiteId/events/stats`
- **Base URL:** `https://api.umami.is/v1`
- **Official documentation:** [Get Event Stats](https://docs.umami.is/docs/api/events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `websiteId` | path | `string` | yes | The website ID. |
| `startAt` | query | `number` | yes | Start timestamp in milliseconds. |
| `endAt` | query | `number` | yes | End timestamp in milliseconds. |
| `compare` | query | `string` | no | Comparison period. Accepted values: `0`, `1`. |
