# Import Recipient with MailUp

Imports a recipient into a MailUp list.

## Endpoint

- **Method:** `POST`
- **Path:** `Console/List/:id_List/Recipient`
- **Base URL:** `https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc`
- **Official documentation:** [Import Recipient](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/AsyncImportRecipientToList)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id_List` | path | `number` | yes |
| `Email` | body | `string` | yes |
| `Name` | body | `string` | no |
| `MobileNumber` | body | `string` | no |
| `MobilePrefix` | body | `string` | no |
