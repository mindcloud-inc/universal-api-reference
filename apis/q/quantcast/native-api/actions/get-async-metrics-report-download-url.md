# Get Async Metrics Report Download URL with Quantcast

Retrieves an async metrics report download URL from Quantcast.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/graphql`
- **Base URL:** `https://developers.quantcast.com`
- **Official documentation:** [Get Async Metrics Report Download URL](https://developers.quantcast.com/docs/graphql-api/reference/queries/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity` | body | `string` | yes | GraphQL EntityInput literal, for example {type: ACCOUNT, id: 123}. |
| `reportRequestId` | body | `number` | yes | Async report request ID returned by Quantcast. |
