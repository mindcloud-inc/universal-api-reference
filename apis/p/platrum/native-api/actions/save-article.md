# Save article with Platrum

Creates or updates a knowledge article in Platrum.

## Endpoint

- **Method:** `POST`
- **Path:** `/wiki/api/article/save`
- **Base URL:** `https://3e8e7be.platrum.com`
- **Official documentation:** [Save article](http://api.docs.platrum.ru/modules/wiki/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `access_comment[]` | body | `array<object>` | no | Comment access rules. |
| `access_edit[]` | body | `array<object>` | no | Edit access rules. |
| `access[]` | body | `array<object>` | no | View access rules. |
| `content_blocks[]` | body | `array<object>` | yes | Article content blocks. |
| `id` | body | `number` | no | Article ID for updates. |
| `parent_ids[]` | body | `array<number>` | no | Parent article IDs. |
| `slug` | body | `string` | no | Article slug. |
| `space_ids[]` | body | `array<number>` | yes | Target space IDs. |
| `title` | body | `string` | no | Article title. |
