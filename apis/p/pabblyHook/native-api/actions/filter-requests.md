# Filter Requests with Pabbly Hook

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/requests`
- **Base URL:** `https://hook.pabbly.com`
- **Official documentation:** [Filter Requests](https://apidocs.pabbly.com/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `connection_id` | query | `string` | no | Connection ID selector. |
| `requestId` | query | `string` | no | Request ID selector. |
| `status` | query | `string` | no | Request status selector. |
| `dateRange` | query | `string` | no | Date range selector, for example YYYY-MM-DD,YYYY-MM-DD. |
