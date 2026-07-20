# Get Weekly Sessions with Umami

## Endpoint

- **Method:** `GET`
- **Path:** `/websites/:websiteId/sessions/weekly`
- **Base URL:** `https://api.umami.is/v1`
- **Official documentation:** [Get Weekly Sessions](https://docs.umami.is/docs/api/sessions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `websiteId` | path | `string` | yes | The website ID. |
| `startAt` | query | `number` | yes | Start timestamp in milliseconds. |
| `endAt` | query | `number` | yes | End timestamp in milliseconds. |
| `timezone` | query | `string` | yes | Timezone like America/Los_Angeles. |
