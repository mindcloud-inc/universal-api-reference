# List Inbox Messages with Microsoft 365 Outlook

Retrieves inbox messages from Microsoft 365 Outlook.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/me/mailFolders/inbox/messages`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [List Inbox Messages](https://learn.microsoft.com/en-us/graph/api/mailfolder-list-messages?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$top` | query | `number` | no | Number of newest inbox messages to return. |
