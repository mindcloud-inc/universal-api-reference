# Generate Custom Thank You Email with SharpAPI

Creates a thank you email job in SharpAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/ecommerce/thank_you_email`
- **Base URL:** `https://sharpapi.com/api/v1`
- **Official documentation:** [Generate Custom Thank You Email](https://sharpapi.com/en/catalog/ai/e-commerce/custom-thank-you-e-mail-generator)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Product name and its parameters to generate the thank you email. |
| `language` | body | `string` | no | Specify the language of the output, defaults to English. |
| `max_length` | body | `number` | no | Specify the maximum length of the email in words. |
| `voice_tone` | body | `string` | no | Specify the voice tone of the output. It can be adjectives like funny or joyous, or even the name of a famous writer. |
| `context` | body | `string` | no | An additional flexible instructions for content processing. |
