# Create List with MailUp

Creates a new list in MailUp.

## Endpoint

- **Method:** `POST`
- **Path:** `Console/List`
- **Base URL:** `https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc`
- **Official documentation:** [Create List](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/CreateNewList)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `Address` | body | `string` | no |
| `City` | body | `string` | no |
| `CompanyName` | body | `string` | no |
| `ContactName` | body | `string` | no |
| `CountryCode` | body | `string` | no |
| `Name` | body | `string` | yes |
| `NLSenderName` | body | `string` | no |
| `PermissionReminder` | body | `string` | no |
| `WebSiteUrl` | body | `string` | no |
| `OwnerEmail` | body | `string` | no |
| `ReplyTo` | body | `string` | no |
| `DisplayAs` | body | `string` | no |
| `Description` | body | `string` | no |
| `Business` | body | `boolean` | no |
| `Customer` | body | `boolean` | no |
| `UseDefaultSettings` | body | `boolean` | no |
| `IdSettings` | body | `number` | no |
| `CopyFromWebhooks` | body | `boolean` | no |
