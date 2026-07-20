# Get Website Stats with Umami

## Endpoint

- **Method:** `GET`
- **Path:** `/websites/:websiteId/stats`
- **Base URL:** `https://api.umami.is/v1`
- **Official documentation:** [Get Website Stats](https://docs.umami.is/docs/api/website-stats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `websiteId` | path | `string` | yes | The website ID. |
| `startAt` | query | `number` | yes | Start timestamp in milliseconds. |
| `endAt` | query | `number` | yes | End timestamp in milliseconds. |
