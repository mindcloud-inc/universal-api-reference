# Get Email with MailUp

Retrieves an email message from MailUp.

## Endpoint

- **Method:** `GET`
- **Path:** `Console/List/:id_List/Email/:id_Message`
- **Base URL:** `https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc`
- **Official documentation:** [Get Email](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/GetMessageDetails)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id_List` | path | `number` | yes |
| `id_Message` | path | `number` | yes |
