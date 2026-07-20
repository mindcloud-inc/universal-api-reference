# Import Recipients with MailUp

Imports recipients into a MailUp list.

## Endpoint

- **Method:** `POST`
- **Path:** `Console/List/:id_List/Recipients`
- **Base URL:** `https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc`
- **Official documentation:** [Import Recipients](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/AsyncImportRecipientsToList)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_List` | path | `number` | yes | — |
| `Recipients` | body | `object` | yes | JSON array of MailUp recipient objects. Each item should use MailUp keys such as Email, Name, MobileNumber, and MobilePrefix. |
