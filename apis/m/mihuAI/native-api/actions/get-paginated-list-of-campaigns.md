# Get Paginated List of Campaigns with Mihu AI

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/campaigns`
- **Base URL:** `https://{subdomain}.mindhunters.ai`
- **Official documentation:** [Get Paginated List of Campaigns](https://developers.mihu.ai/api-reference/campaigns/get-paginated-list-of-campaigns)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `page` | query | `number` | no |
| `per_page` | query | `number` | no |
| `search` | query | `string` | no |
| `status` | query | `string` | no |
