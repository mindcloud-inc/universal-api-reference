# List Unsubscribed Recipients with MailUp

Retrieves unsubscribed recipients from a MailUp list.

## Endpoint

- **Method:** `GET`
- **Path:** `Console/List/:id_List/Recipients/Unsubscribed`
- **Base URL:** `https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc`
- **Official documentation:** [List Unsubscribed Recipients](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/GetUnsubscribedRecipientsByList)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id_List` | path | `number` | yes |
