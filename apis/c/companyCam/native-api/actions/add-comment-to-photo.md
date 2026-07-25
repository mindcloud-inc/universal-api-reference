# Add Comment to Photo with CompanyCam

## Endpoint

- **Method:** `POST`
- **Path:** `photos/:id/comments`
- **Base URL:** `https://api.companycam.com/v2/`
- **Official documentation:** [Add Comment to Photo](https://docs.companycam.com/reference/createphotocomment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `comment.content` | body | `string` | no | Enter the comment text here. |
| `id` | path | `string` | yes | ID of the Photo |
| `comment` | body | `object` | no | — |
