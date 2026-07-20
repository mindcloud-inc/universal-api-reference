# Update Group with Bitly

Updates an existing group in Bitly.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/groups/:group_guid`
- **Base URL:** `https://api-ssl.bitly.com/v4`
- **Official documentation:** [Update Group](https://dev.bitly.com/api-reference#updateGroup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bsds[]` | body | `array<string>` | no | The branded short domains assigned to the group. |
| `group_guid` | path | `string` | yes | The Bitly group GUID. |
| `name` | body | `string` | no | The updated group name. |
| `organization_guid` | body | `string` | no | The organization GUID for the group. |
