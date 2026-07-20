# List Campaigns with Vapi

Retrieves a list of campaigns from Vapi.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaign`
- **Base URL:** `https://api.vapi.ai`
- **Official documentation:** [List Campaigns](https://docs.vapi.ai/api-reference/campaigns/campaign-controller-find-all)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | no | — |
| `status` | query | `string` | no | — |
| `page` | query | `number` | no | This is the page number to return. Defaults to 1. |
| `sortOrder` | query | `string` | no | This is the sort order for pagination. Defaults to 'DESC'. |
| `limit` | query | `number` | no | This is the maximum number of items to return. Defaults to 100. |
| `createdAtGt` | query | `string` | no | This will return items where the createdAt is greater than the specified value. |
| `createdAtLt` | query | `string` | no | This will return items where the createdAt is less than the specified value. |
| `createdAtGe` | query | `string` | no | This will return items where the createdAt is greater than or equal to the specified value. |
| `createdAtLe` | query | `string` | no | This will return items where the createdAt is less than or equal to the specified value. |
| `updatedAtGt` | query | `string` | no | This will return items where the updatedAt is greater than the specified value. |
| `updatedAtLt` | query | `string` | no | This will return items where the updatedAt is less than the specified value. |
| `updatedAtGe` | query | `string` | no | This will return items where the updatedAt is greater than or equal to the specified value. |
| `updatedAtLe` | query | `string` | no | This will return items where the updatedAt is less than or equal to the specified value. |
