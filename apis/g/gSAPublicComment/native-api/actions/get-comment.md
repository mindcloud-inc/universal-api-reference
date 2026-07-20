# Get Comment with GSA Public Comment

Retrieves a specific comment from GSA Public Comment.

## Endpoint

- **Method:** `GET`
- **Path:** `/comments/:commentId`
- **Base URL:** `https://api.regulations.gov/v4`
- **Official documentation:** [Get Comment](https://open.gsa.gov/api/regulationsgov/#detailed-information-for-a-single-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `commentId` | path | `string` | yes | ID of the comment to return. |
| `include` | query | `string` | no | Use attachments to include attachments in the response. |
