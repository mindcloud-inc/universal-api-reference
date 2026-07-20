# Get Session Stats with Umami

## Endpoint

- **Method:** `GET`
- **Path:** `/websites/:websiteId/sessions/stats`
- **Base URL:** `https://api.umami.is/v1`
- **Official documentation:** [Get Session Stats](https://docs.umami.is/docs/api/sessions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `websiteId` | path | `string` | yes | The website ID. |
| `startAt` | query | `number` | yes | Timestamp in milliseconds for the start of the reporting range. |
| `endAt` | query | `number` | yes | Timestamp in milliseconds for the end of the reporting range. |
