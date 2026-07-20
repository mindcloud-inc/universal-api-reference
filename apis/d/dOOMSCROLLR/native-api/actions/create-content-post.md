# Create Content Post with DOOMSCROLLR

## Endpoint

- **Method:** `POST`
- **Path:** `/api/content/posts`
- **Base URL:** `https://mindcloudapps0402.doomscrollr.com`
- **Official documentation:** [Create Content Post](https://doomscrollr.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Public URL of the post content to publish in DOOMSCROLLR. |
| `title` | body | `string` | no | Title of the content post. |
| `description` | body | `string` | no | Description text for the content post. |
| `status` | body | `string` | no | Publish status for the new content post. |
| `tags[]` | body | `array<string>` | no | Tags to associate with the content post. Send multiple values as a array. |
