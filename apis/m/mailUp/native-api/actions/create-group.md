# Create Group with MailUp

Creates a new group in a MailUp list.

## Endpoint

- **Method:** `POST`
- **Path:** `Console/List/:id_List/Group`
- **Base URL:** `https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc`
- **Official documentation:** [Create Group](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/CreateGroup)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id_List` | path | `number` | yes |
| `Name` | body | `string` | yes |
| `Notes` | body | `string` | no |
