# Get Website Metrics with Umami

## Endpoint

- **Method:** `GET`
- **Path:** `/websites/:websiteId/metrics`
- **Base URL:** `https://api.umami.is/v1`
- **Official documentation:** [Get Website Metrics](https://docs.umami.is/docs/api/website-stats)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `websiteId` | path | `string` | yes | The website ID. |
| `startAt` | query | `number` | yes | Start timestamp in milliseconds. |
| `endAt` | query | `number` | yes | End timestamp in milliseconds. |
| `type` | query | `string` | no | Metric type to group by. Accepted values: `0`, `1`, `10`, `11`, `12`, `13`, `14`, `15`, `16`, `17`, `18`, `19`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |
