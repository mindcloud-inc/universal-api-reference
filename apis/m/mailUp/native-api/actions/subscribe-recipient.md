# Subscribe Recipient with MailUp

Subscribes a recipient to a MailUp list.

## Endpoint

- **Method:** `POST`
- **Path:** `Console/List/:id_List/Subscribe/:id_Recipient`
- **Base URL:** `https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc`
- **Official documentation:** [Subscribe Recipient](https://services.mailup.com/API/v1.1/Rest/ConsoleService.svc/help/operations/SubscribeRecipientToList)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id_List` | path | `number` | yes |
| `id_Recipient` | path | `number` | yes |
