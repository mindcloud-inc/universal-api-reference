# Update a story with Asana

Updates a story in Asana.

## Endpoint

- **Method:** `PUT`
- **Path:** `stories/:story_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Update a story](https://developers.asana.com/reference/updatestory)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `string` | yes | — |
| `story_gid` | path | `string` | yes | Asana story gid parameter. |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `opt_fields` | query | `list<string>` | no | Asana opt fields parameter. |
| `data.gid` | body | `string` | no | Asana gid parameter. |
| `data.resource_type` | body | `string` | no | Asana resource type parameter. |
| `data.created_at` | body | `string` | no | Asana created at parameter. |
| `data.resource_subtype` | body | `string` | no | Asana resource subtype parameter. |
| `data.text` | body | `string` | no | Asana text parameter. |
| `data.html_text` | body | `string` | no | Asana html text parameter. |
| `data.is_pinned` | body | `boolean` | no | Asana is pinned parameter. |
| `data.sticker_name` | body | `string` | no | Asana sticker name parameter. |
