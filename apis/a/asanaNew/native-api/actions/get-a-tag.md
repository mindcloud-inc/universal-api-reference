# Get a tag with Asana

Retrieves a tag from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `tags/:tag_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get a tag](https://developers.asana.com/reference/gettag)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tag_gid` | path | `string` | yes | Asana tag gid parameter. |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `opt_fields` | query | `list<string>` | no | Asana opt fields parameter. |
