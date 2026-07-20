# Delete a tag with Asana

Deletes a tag from Asana.

## Endpoint

- **Method:** `DELETE`
- **Path:** `tags/:tag_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Delete a tag](https://developers.asana.com/reference/deletetag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tag_gid` | path | `string` | yes | Asana tag gid parameter. |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
