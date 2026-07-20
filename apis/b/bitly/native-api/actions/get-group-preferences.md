# Get Group Preferences with Bitly

Retrieves group preferences from your Bitly account.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups/:group_guid/preferences`
- **Base URL:** `https://api-ssl.bitly.com/v4`
- **Official documentation:** [Get Group Preferences](https://dev.bitly.com/api-reference#getGroupPreferences)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_guid` | path | `string` | yes | The Bitly group GUID. |
