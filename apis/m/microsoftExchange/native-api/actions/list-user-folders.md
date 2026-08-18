# List User Folders with Microsoft Exchange

Finds messages in a user's mailbox.

## Endpoint

- **Method:** `GET`
- **Path:** `https://graph.microsoft.com/v1.0/users/:userIdOrPrincipalName/mailFolders`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [List User Folders](https://learn.microsoft.com/en-us/graph/api/mailfolder-get?view=graph-rest-1.0&tabs=http)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userIdOrPrincipalName` | path | `string` | yes | The Microsoft Graph user id or userPrincipalName for the mailbox whose folder messages should be listed. Use the Entra user id when the mail address differs from the userPrincipalName. |
| `$top` | query | `number` | no | Maximum number of messages to return. |
| `$select` | query | `string` | no | Comma-separated Microsoft Graph message fields to return. |
| `$filter` | query | `string` | no | Optional Microsoft Graph OData filter expression. |
| `$count` | query | `string` | no | — |
