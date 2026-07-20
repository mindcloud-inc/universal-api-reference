# Update List with MailUp

Updates an existing list in MailUp.

## Endpoint

- **Method:** `PUT`
- **Path:** `Console/List/:id_List`
- **Base URL:** `https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc`
- **Official documentation:** [Update List](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/UpdateExistingList)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id_List` | path | `number` | yes |
| `NLSenderName` | body | `string` | no |
| `WebSiteUrl` | body | `string` | no |
| `Name` | body | `string` | yes |
| `OwnerEmail` | body | `string` | no |
| `ReplyTo` | body | `string` | no |
| `DisplayAs` | body | `string` | no |
| `Description` | body | `string` | no |
| `Business` | body | `boolean` | no |
| `Customer` | body | `boolean` | no |
| `CompanyName` | body | `string` | no |
| `ContactName` | body | `string` | no |
| `Phone` | body | `string` | no |
| `Address` | body | `string` | no |
| `City` | body | `string` | no |
| `PostalCode` | body | `string` | no |
| `StateOrProvince` | body | `string` | no |
| `CountryCode` | body | `string` | no |
| `PermissionReminder` | body | `string` | no |
