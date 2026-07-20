# Request Async Metrics Report with Quantcast

Requests an async metrics report from Quantcast.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/graphql`
- **Base URL:** `https://developers.quantcast.com`
- **Official documentation:** [Request Async Metrics Report](https://developers.quantcast.com/docs/graphql-api/reference/queries/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `metricsReportRequest` | body | `string` | yes | GraphQL input object literal for the async metrics report request. |
| `fileName` | body | `string` | no | Optional filename for the exported report. |
