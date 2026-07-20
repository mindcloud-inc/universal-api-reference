# Update Post with Typlog

## Endpoint

- **Method:** `PUT`
- **Path:** `/posts/[:id]`
- **Base URL:** `https://api.typlog.com/v3`
- **Official documentation:** [Update Post](https://api.typlog.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the post. |
| `siteId` | query | `number` | yes | Typlog site ID used to set the X-Site-Id header. |
| `title` | body | `string` | yes | Post title. |
| `slug` | body | `string` | yes | Post slug. |
| `lang` | body | `string` | yes | Post language code. |
| `format` | body | `string` | yes | Post content format. |
| `subtitle` | body | `string` | no | Post subtitle. |
| `visibility` | body | `string` | no | Post visibility. |
| `comment` | body | `string` | no | Comment setting. |
| `tags[]` | body | `array<number>` | no | Tag IDs. |
| `primary_authors[]` | body | `array<number>` | no | Primary author IDs. |
| `secondary_authors[]` | body | `array<number>` | no | Secondary author IDs. |
