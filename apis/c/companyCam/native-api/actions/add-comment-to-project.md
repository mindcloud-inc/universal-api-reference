# Add Comment to Project with CompanyCam

## Endpoint

- **Method:** `POST`
- **Path:** `projects/:id/comments`
- **Base URL:** `https://api.companycam.com/v2/`
- **Official documentation:** [Add Comment to Project](https://docs.companycam.com/reference/createprojectcomment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `comment.content` | body | `string` | no | Enter the comment text here. |
| `id` | path | `string` | yes | ID of the Project |
| `comment` | body | `object` | no | — |
