# Update Note with Swipe One

## Endpoint

- **Method:** `PATCH`
- **Path:** `/notes/:noteId`
- **Base URL:** `https://api.swipeone.com/api`
- **Official documentation:** [Update Note](https://docs.swipeone.com/en/articles/10546101-notes#h_80ff056a23)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `noteId` | path | `string` | yes | Note to update. |
| `title` | body | `string` | no | Updated note title. |
| `content` | body | `string` | no | Updated note content. |
