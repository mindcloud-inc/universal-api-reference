# List Contact Notes with Swipe One

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts/:contactId/notes`
- **Base URL:** `https://api.swipeone.com/api`
- **Official documentation:** [List Contact Notes](https://docs.swipeone.com/en/articles/10546101-notes#h_84e41e006a)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | Contact whose notes should be listed. |
| `page` | query | `number` | no | Page number. |
| `limit` | query | `number` | no | Number of records per page. |
