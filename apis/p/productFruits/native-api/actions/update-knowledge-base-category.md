# Update Knowledge Base Category with Product Fruits

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/knowledgebase/categories/:correlationId`
- **Base URL:** `https://api.productfruits.com`
- **Official documentation:** [Update Knowledge Base Category](https://help.productfruits.com/en/article/knowledge-base-api-update-specific-category)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contents[]` | body | `array<object>` | no | Array of localized category content objects. |
| `correlationId` | path | `string` | yes | The correlation ID of the category to update. |
| `icon` | body | `string` | no | Category icon or CDN image GUID. |
| `isFeatured` | body | `boolean` | no | Whether the category is featured. |
| `order` | body | `number` | no | Display order within the parent category. |
| `parentCategoryId` | body | `number` | no | Parent category ID. Use null for a root category. |
