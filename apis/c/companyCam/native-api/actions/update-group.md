# Update Group with CompanyCam

## Endpoint

- **Method:** `PUT`
- **Path:** `groups/:id`
- **Base URL:** `https://api.companycam.com/v2/`
- **Official documentation:** [Update Group](https://docs.companycam.com/reference/updategroup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group.name` | body | `string` | no | The title of the Group |
| `id` | path | `string` | yes | ID of the Group |
| `group` | body | `object` | no | — |
| `group.users` | body | `list<string>` | no | An array of strings containing the UserIDs to add to this group. Send multiple values as a array. |
