# Create Group with CompanyCam

## Endpoint

- **Method:** `POST`
- **Path:** `groups`
- **Base URL:** `https://api.companycam.com/v2/`
- **Official documentation:** [Create Group](https://docs.companycam.com/reference/creategroup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group` | body | `object` | no | — |
| `group.name` | body | `string` | no | The title of the Group |
| `group.users` | body | `list<string>` | no | An array of strings containing the UserIDs to add to this group. Send multiple values as a array. |
