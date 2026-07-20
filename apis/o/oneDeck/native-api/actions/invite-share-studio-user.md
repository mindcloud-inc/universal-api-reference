# Invite Share Studio User with OneDeck

Invites a user to OneDeck Share Studio.

## Endpoint

- **Method:** `POST`
- **Path:** `/share-studio/:shareId/invite`
- **Base URL:** `https://{accountName}.onedeck.com/api/v1`
- **Official documentation:** [Invite Share Studio User](https://www.onedeck.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shareId` | path | `string` | yes | Share Studio identifier. |
| `email` | body | `string` | yes | Email address to invite. |
| `firstName` | body | `string` | no | Invitee first name. |
| `lastName` | body | `string` | no | Invitee last name. |
| `recordId` | body | `string` | no | Record identifier to scope the invitation. |
