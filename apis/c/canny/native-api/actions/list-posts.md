# List Posts with Canny

Retrieves all available posts from Canny.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/posts/list`
- **Base URL:** `https://canny.io/api`
- **Official documentation:** [List Posts](https://developers.canny.io/api-reference#list_posts)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `boardID` | body | `string` | no |
| `authorID` | body | `string` | no |
| `companyID` | body | `string` | no |
| `tagIDs` | body | `list<string>` | no |
| `search` | body | `string` | no |
| `status` | body | `string` | no |
| `sort` | body | `string` | no |
| `limit` | body | `number` | no |
| `skip` | body | `number` | no |
