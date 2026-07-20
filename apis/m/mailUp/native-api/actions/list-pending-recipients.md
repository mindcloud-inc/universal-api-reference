# List Pending Recipients with MailUp

Retrieves pending recipients from a MailUp list.

## Endpoint

- **Method:** `GET`
- **Path:** `Console/List/:id_List/Recipients/Pending`
- **Base URL:** `https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc`
- **Official documentation:** [List Pending Recipients](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/GetPendingRecipientsByList)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id_List` | path | `number` | yes |
