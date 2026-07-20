# Update Group Preferences with Bitly

Updates existing group preferences in Bitly.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/groups/:group_guid/preferences`
- **Base URL:** `https://api-ssl.bitly.com/v4`
- **Official documentation:** [Update Group Preferences](https://dev.bitly.com/api-reference#updateGroupPreferences)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain_preference` | body | `string` | no | The preferred domain setting for the group. |
| `group_guid` | path | `string` | yes | The Bitly group GUID. |
