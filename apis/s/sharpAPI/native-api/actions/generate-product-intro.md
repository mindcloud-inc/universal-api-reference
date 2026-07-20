# Generate Product Intro with SharpAPI

Creates a product intro job in SharpAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/ecommerce/product_intro`
- **Base URL:** `https://sharpapi.com/api/v1`
- **Official documentation:** [Generate Product Intro](https://sharpapi.com/en/catalog/ai/e-commerce/product-intro-generator)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Product name and its parameters to generate the product intro. |
| `language` | body | `string` | no | Specify the language of the output, defaults to English. |
| `max_length` | body | `number` | no | Specify the maximum length of the intro in number of words. |
| `voice_tone` | body | `string` | no | Specify the voice tone of the output. It can be adjectives like funny or joyous, or even the name of a famous writer. |
