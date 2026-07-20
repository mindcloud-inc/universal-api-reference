# List Posts with Late

## Endpoint

- **Method:** `GET`
- **Path:** `/posts`
- **Base URL:** `https://zernio.com/api/v1`
- **Official documentation:** [List Posts](https://docs.zernio.com/posts/list-posts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `list<string>` | no | Filter posts by status. Accepted values: `draft`, `failed`, `published`, `scheduled`. |
| `platform` | query | `string` | no | Filter posts by platform. |
| `profileId` | query | `string` | no | Filter posts by profile ID. |
| `createdBy` | query | `string` | no | Filter posts by creator ID. |
| `dateFrom` | query | `date` | no | Return posts created on or after this date. |
| `dateTo` | query | `date` | no | Return posts created on or before this date. |
| `includeHidden` | query | `boolean` | no | When true, include hidden posts. |
| `search` | query | `string` | no | Search posts by text content. |
| `sortBy` | query | `list<string>` | no | Sort order for results. Accepted values: `created-asc`, `created-desc`, `platform`, `scheduled-asc`, `scheduled-desc`, `status`. |
