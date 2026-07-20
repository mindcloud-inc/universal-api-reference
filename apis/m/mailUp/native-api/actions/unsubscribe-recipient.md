# Unsubscribe Recipient with MailUp

Unsubscribes a recipient from a MailUp list.

## Endpoint

- **Method:** `DELETE`
- **Path:** `Console/List/:id_List/Unsubscribe/:id_Recipient`
- **Base URL:** `https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc`
- **Official documentation:** [Unsubscribe Recipient](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/RemoveRecipientFromList)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id_List` | path | `number` | yes |
| `id_Recipient` | path | `number` | yes |
