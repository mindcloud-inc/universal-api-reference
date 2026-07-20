# Categorize Tours Activities Product with SharpAPI

Creates a tours activities categorization job in SharpAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/tth/ta_product_categories`
- **Base URL:** `https://sharpapi.com/api/v1`
- **Official documentation:** [Categorize Tours Activities Product](https://sharpapi.com/en/catalog/ai/travel-tourism-hospitality/tours-activities-product-categorization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Provide the content to generate travel product categories. |
| `city` | body | `string` | no | Specify the city of travel. |
| `country` | body | `string` | no | Specify the country related to travel. |
| `language` | body | `string` | no | Specify the language of the output, defaults to English. |
| `max_quantity` | body | `number` | no | Specify the maximum number of product categories to generate. |
| `voice_tone` | body | `string` | no | Specify the voice tone of the output. |
| `context` | body | `string` | no | The list of other categories that will be taken into consideration during the mapping process. |
