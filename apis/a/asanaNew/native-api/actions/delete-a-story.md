# Delete a story with Asana

Deletes a story from Asana.

## Endpoint

- **Method:** `DELETE`
- **Path:** `stories/:story_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Delete a story](https://developers.asana.com/reference/deletestory)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `story_gid` | path | `string` | yes |
| `opt_pretty` | query | `boolean` | no |
