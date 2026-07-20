# Update Episode with Typlog

## Endpoint

- **Method:** `PUT`
- **Path:** `/episodes/[:id]`
- **Base URL:** `https://api.typlog.com/v3`
- **Official documentation:** [Update Episode](https://api.typlog.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the episode. |
| `siteId` | query | `number` | yes | Typlog site ID used to set the X-Site-Id header. |
| `title` | body | `string` | yes | Episode title. |
| `slug` | body | `string` | yes | Episode slug. |
| `lang` | body | `string` | yes | Episode language code. |
| `format` | body | `string` | yes | Episode content format. |
| `subtitle` | body | `string` | no | Episode subtitle. |
| `visibility` | body | `string` | no | Episode visibility. |
| `comment` | body | `string` | no | Comment setting. |
| `season` | body | `number` | no | Season number. |
| `episode` | body | `number` | no | Episode number. |
| `explicit` | body | `boolean` | no | Whether the episode is explicit. |
| `episode_type` | body | `string` | no | Episode type. |
| `tags[]` | body | `array<number>` | no | Tag IDs. |
| `hosts[]` | body | `array<number>` | no | Host author IDs. |
| `guests[]` | body | `array<number>` | no | Guest author IDs. |
