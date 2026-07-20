# Get Email Send History with MailUp

Retrieves send history for a MailUp email.

## Endpoint

- **Method:** `GET`
- **Path:** `Console/List/:id_List/Email/:id_Message/SendHistory`
- **Base URL:** `https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc`
- **Official documentation:** [Get Email Send History](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/GetMailMessageSendHistory)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id_List` | path | `number` | yes |
| `id_Message` | path | `number` | yes |
