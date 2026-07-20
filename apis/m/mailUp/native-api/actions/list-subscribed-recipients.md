# List Subscribed Recipients with MailUp

Retrieves subscribed recipients from a MailUp list.

## Endpoint

- **Method:** `GET`
- **Path:** `Console/List/:id_List/Recipients/Subscribed`
- **Base URL:** `https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc`
- **Official documentation:** [List Subscribed Recipients](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/GetSubscribedRecipientsByList)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id_List` | path | `number` | yes |
