# Get Paginated List of Calls with Mihu AI

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/calls`
- **Base URL:** `https://{subdomain}.mindhunters.ai`
- **Official documentation:** [Get Paginated List of Calls](https://developers.mihu.ai/api-reference/call/get-paginated-list-of-calls)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | query | `string` | no | Filter calls by agent UUID. |
| `direction` | query | `string` | no | Filter calls by call direction. |
| `page` | query | `number` | no | Page number to return. |
| `per_page` | query | `number` | no | Number of records to return per page. |
| `status` | query | `string` | no | Filter calls by status. |
