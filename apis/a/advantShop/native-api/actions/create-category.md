# Create Category with AdvantShop

Creates a new category in AdvantShop.

## Endpoint

- **Method:** `POST`
- **Path:** `/categories/add`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Create Category](https://www.advantshop.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Name` | body | `string` | yes | Category name. |
| `ParentCategoryId` | body | `number` | no | Optional parent category identifier. |
