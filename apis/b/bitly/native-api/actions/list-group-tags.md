# List Group Tags with Bitly

Retrieves tags for a group in Bitly.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups/:group_guid/tags`
- **Base URL:** `https://api-ssl.bitly.com/v4`
- **Official documentation:** [List Group Tags](https://dev.bitly.com/api-reference#getGroupTags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_guid` | path | `string` | yes | The Bitly group GUID. |
| `type` | query | `string` | no | Filter tags by resource type. |
