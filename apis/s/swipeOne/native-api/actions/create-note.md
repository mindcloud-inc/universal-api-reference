# Create Note with Swipe One

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/:contactId/notes`
- **Base URL:** `https://api.swipeone.com/api`
- **Official documentation:** [Create Note](https://docs.swipeone.com/en/articles/10546101-notes#h_ba74b59a4f)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | The unique ID of the contact for which the note is created. |
| `title` | body | `string` | yes | The title of the note. |
| `content` | body | `string` | yes | The content of the note. |
