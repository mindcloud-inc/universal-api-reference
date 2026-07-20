# Create Email with MailUp

Creates a new email message in MailUp.

## Endpoint

- **Method:** `POST`
- **Path:** `Console/List/:id_List/Email`
- **Base URL:** `https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc`
- **Official documentation:** [Create Email](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/CreateEmailMessage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id_List` | path | `number` | yes | — |
| `Subject` | body | `string` | yes | — |
| `Content` | body | `string` | yes | — |
| `Notes` | body | `string` | no | — |
| `Structure` | body | `string` | no | — |
| `UseDynamicField` | body | `boolean` | no | — |
| `Embed` | body | `boolean` | no | — |
| `IsConfirmation` | body | `boolean` | no | — |
| `PreHeader` | body | `string` | no | — |
| `TrackingInfo` | body | `object` | yes | MailUp tracking configuration object, for example {"Enabled":true,"Protocols":["http:","https:","ftp:","news:"],"CustomParams":""}. |
