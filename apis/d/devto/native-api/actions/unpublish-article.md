# Unpublish Article with Dev.to

Unpublishes a Dev.to article by ID.

## Endpoint

- **Method:** `PUT`
- **Path:** `/articles/:id/unpublish`
- **Base URL:** `https://dev.to/api`
- **Official documentation:** [Unpublish Article](https://developers.forem.com/api/v1#tag/articles/operation/unpublishArticle)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Numeric article ID to unpublish. |
| `note` | query | `string` | no | Optional note recorded when unpublishing the article. |
