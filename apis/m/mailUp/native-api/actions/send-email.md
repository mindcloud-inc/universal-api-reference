# Send Email with MailUp

Sends an email message to a MailUp list.

## Endpoint

- **Method:** `POST`
- **Path:** `Console/List/:id_List/Email/:id_Message/Send`
- **Base URL:** `https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc`
- **Official documentation:** [Send Email](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/SendMailMessageToRecipientInList)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id_List` | path | `number` | yes |
| `id_Message` | path | `number` | yes |
