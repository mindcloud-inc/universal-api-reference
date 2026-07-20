# Get Event Series with Umami

## Endpoint

- **Method:** `GET`
- **Path:** `/websites/:websiteId/events/series`
- **Base URL:** `https://api.umami.is/v1`
- **Official documentation:** [Get Event Series](https://docs.umami.is/docs/api/website-stats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `websiteId` | path | `string` | yes | The website ID. |
| `startAt` | query | `number` | yes | Start timestamp in milliseconds. |
| `endAt` | query | `number` | yes | End timestamp in milliseconds. |
| `unit` | query | `string` | no | Time bucket unit. Accepted values: `0`, `1`, `2`, `3`. |
| `timezone` | query | `string` | yes | Timezone like America/Los_Angeles. |
