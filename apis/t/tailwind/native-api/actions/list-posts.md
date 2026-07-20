# List Posts with Tailwind

Retrieves posts from Tailwind.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/accounts/:accountId/posts`
- **Base URL:** `https://api-v1.tailwind.ai`
- **Official documentation:** [List Posts](https://api-docs.tailwind.ai/rest-api/operations/v1accountsaccountidposts/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | Pinterest account ID. |
| `status` | query | `string` | no | Filter by post status. Defaults to queued. Accepted values: `0`, `1`, `2`, `3`. |
| `cursor` | query | `string` | no | Pagination cursor from a previous response. |
| `startDate` | query | `date` | no | Filter posts scheduled after this ISO 8601 date-time. Required by Tailwind when status is sent or uploading. |
| `endDate` | query | `date` | no | Filter posts scheduled before this ISO 8601 date-time. Required by Tailwind when status is sent or uploading. |
