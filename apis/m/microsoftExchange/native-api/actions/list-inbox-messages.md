# List Inbox Messages with Microsoft Exchange

Finds inbox messages in Microsoft Exchange by newest first.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/me/mailFolders/inbox/messages`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [List Inbox Messages](https://learn.microsoft.com/en-us/graph/api/mailfolder-list-messages?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$top` | query | `number` | no | Number of newest inbox messages to return. |
