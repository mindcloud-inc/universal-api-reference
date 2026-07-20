# List Chat Members with Zoho Cliq

Retrieves members of a Zoho Cliq chat.

## Endpoint

- **Method:** `GET`
- **Path:** `/chats/:chatId/members`
- **Base URL:** `https://cliq.zoho.com/api/v2`
- **Official documentation:** [List Chat Members](https://www.zoho.com/cliq/help/restapi/v2/#retrieve-members)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chatId` | path | `string` | yes | The ID of the chat whose members should be retrieved. |
| `fields` | query | `string` | no | Comma-separated member fields to include, such as name or email. |
