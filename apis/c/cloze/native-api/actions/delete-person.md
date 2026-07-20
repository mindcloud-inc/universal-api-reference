# Delete Person with Cloze

Deletes a person from Cloze.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/people/delete`
- **Base URL:** `https://api.cloze.com`
- **Official documentation:** [Delete Person](https://api.cloze.com/api-docs/#/paths/v1-people-delete/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team` | query | `boolean` | no | Delete the team relation instead of the local relation. |
| `uniqueid` | query | `string` | yes | Person unique identifier such as email address, mobile phone number, or social identifier. |
