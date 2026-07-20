# Create Tag with Nozbe Personal

Creates a new tag in Nozbe Personal.

## Endpoint

- **Method:** `POST`
- **Path:** `/tags`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [Create Tag](https://api4.nozbe.com/v1/api#/tags/postTag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Tag name. |
| `team_id` | body | `string` | no | Optional team that owns the tag. |
| `color` | body | `string` | no | Optional tag color. |
| `icon` | body | `string` | no | Optional tag icon. |
| `is_favorite` | body | `boolean` | no | Whether the tag is a favorite. |
