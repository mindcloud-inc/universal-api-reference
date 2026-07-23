# List Messages in Folder with Microsoft Exchange

Finds messages in a mail folder in Microsoft Exchange.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/me/mailFolders/{{mailFolderId}}/messages`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [List Messages in Folder](https://learn.microsoft.com/en-us/graph/api/mailfolder-list-messages?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mailFolderId` | path | `string` | yes | The mail folder ID or a well-known folder name such as inbox or archive. |
| `$top` | query | `number` | no | Maximum number of messages to return. |
| `$expand` | query | `string` | no | OData expand expression for returning attachment metadata, including inline attachment flags. |
