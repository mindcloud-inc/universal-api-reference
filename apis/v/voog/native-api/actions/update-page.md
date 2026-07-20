# Update Page with Voog

Updates an existing page in the current Voog site.

## Endpoint

- **Method:** `PUT`
- **Path:** `/pages/:pageId`
- **Base URL:** `{siteUrl}/admin/api`
- **Official documentation:** [Update Page](https://www.voog.com/developers/api/resources/pages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageId` | path | `number` | yes | Numeric page ID. |
| `title` | body | `string` | yes | Updated page title. |
