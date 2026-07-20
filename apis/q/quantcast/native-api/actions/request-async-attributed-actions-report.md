# Request Async Attributed Actions Report with Quantcast

Requests an async attributed actions report from Quantcast.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/graphql`
- **Base URL:** `https://developers.quantcast.com`
- **Official documentation:** [Request Async Attributed Actions Report](https://developers.quantcast.com/docs/graphql-api/reference/queries/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attributedActionsReportRequest` | body | `string` | yes | GraphQL input object literal for the async attributed actions report request. |
| `fileName` | body | `string` | no | Optional filename for the exported report. |
