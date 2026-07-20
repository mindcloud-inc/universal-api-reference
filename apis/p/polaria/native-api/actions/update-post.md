# Update Post with Polaria

Updates an existing post in Polaria.

## Endpoint

- **Method:** `PUT`
- **Path:** `/faqs/[:id]`
- **Base URL:** `https://app.polaria.ai/rest/v2`
- **Official documentation:** [Update Post](https://help.polaria.ai/hc/rest-api-posts/put-faqs-id-update-a-post?lang=en)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the post to update. |
| `title` | body | `string` | no | — |
| `content` | body | `string` | no | — |
| `status` | body | `string` | no | — |
| `canned_response` | body | `boolean` | no | — |
| `faq_category_id` | body | `number` | no | — |
| `widgets[]` | body | `array<string>` | no | — |
