# Generate Seo Social Media Tags with SharpAPI

Creates SEO and social media tags in SharpAPI.

## Endpoint

- **Method:** `POST`
- **Path:** `/seo/generate_tags`
- **Base URL:** `https://sharpapi.com/api/v1`
- **Official documentation:** [Generate Seo Social Media Tags](https://sharpapi.com/en/catalog/ai/seo/seo-social-media-tags-generator)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Provide the content to generate SEO tags. |
| `voice_tone` | body | `string` | no | Specify the voice tone of the output. It can be adjectives like funny or joyous, or even the name of a famous writer. |
| `language` | body | `string` | no | Specify the language of the output, defaults to English. |
