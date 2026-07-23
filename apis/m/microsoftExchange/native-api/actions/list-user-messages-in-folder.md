# List User Messages in Folder with Microsoft Exchange

Finds messages in a user's mail folder in Microsoft Exchange.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/users/:userIdOrPrincipalName/mailFolders/:mailFolderId/messages`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [List User Messages in Folder](https://learn.microsoft.com/en-us/graph/api/mailfolder-list-messages?view=graph-rest-1.0&tabs=http)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userIdOrPrincipalName` | path | `string` | yes | The Microsoft Graph user id or userPrincipalName for the mailbox whose folder messages should be listed. Use the Entra user id when the mail address differs from the userPrincipalName. |
| `mailFolderId` | path | `string` | yes | The Microsoft Graph mail folder ID or lowercase well-known folder name, such as inbox or sentitems. If a well-known name is not found for a mailbox, list that user's folders and pass the returned folder id. |
| `$top` | query | `number` | no | Maximum number of messages to return. |
| `$expand` | query | `string` | no | Optional Microsoft Graph $expand expression. The default returns attachment metadata including isInline so inline images can be counted. |
