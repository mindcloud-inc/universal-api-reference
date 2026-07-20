# Categorize Product with SharpAPI

Creates a product categorization job in SharpAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/ecommerce/product_categories`
- **Base URL:** `https://sharpapi.com/api/v1`
- **Official documentation:** [Categorize Product](https://sharpapi.com/en/catalog/ai/e-commerce/product-categorization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Product name and its parameters to generate the categories. |
| `language` | body | `string` | no | Specify the language of the output, defaults to English. |
| `max_quantity` | body | `number` | no | Maximum number of product categories to generate. |
| `voice_tone` | body | `string` | no | Preferred writing style parameter. It can be adjectives like funny or joyous, or even the name of a famous writer. |
| `context` | body | `string` | no | The list of other categories that will be taken into consideration during the mapping process. |
