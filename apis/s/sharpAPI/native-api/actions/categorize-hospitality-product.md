# Categorize Hospitality Product with SharpAPI

Creates a hospitality product categorization job in SharpAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/tth/hospitality_product_categories`
- **Base URL:** `https://sharpapi.com/api/v1`
- **Official documentation:** [Categorize Hospitality Product](https://sharpapi.com/en/catalog/ai/travel-tourism-hospitality/hospitality-product-categorization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Provide the content to generate travel product categories. |
| `city` | body | `string` | no | Specify the city to travel. |
| `country` | body | `string` | no | Specify the country to travel. |
| `language` | body | `string` | no | Specify the language of the output, defaults to English. |
| `max_quantity` | body | `number` | no | Maximum number of product categories to generate. |
| `voice_tone` | body | `string` | no | Specify the voice tone. The default will be neutral. |
| `context` | body | `string` | no | The list of other categories that will be taken into consideration during the mapping process. |
