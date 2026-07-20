# Create Post with Polaria

Creates a new post in Polaria.

## Endpoint

- **Method:** `POST`
- **Path:** `/faqs`
- **Base URL:** `https://app.polaria.ai/rest/v2`
- **Official documentation:** [Create Post](https://help.polaria.ai/hc/rest-api-posts/post-faqs-create-a-post?lang=en)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `title` | body | `string` | yes |
| `content` | body | `string` | yes |
| `status` | body | `string` | no |
| `canned_response` | body | `boolean` | no |
| `faq_category_id` | body | `number` | no |
| `widgets[]` | body | `array<string>` | no |
| `language` | body | `string` | no |
