# Add Comment with Sprinklr

Creates a comment in Sprinklr.

## Endpoint

- **Method:** `POST`
- **Path:** `api/v2/comment/{entityType}/{entityId}`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Add Comment](https://dev.sprinklr.com/docs/prod4/1/routes/api%2Fv2%2Fcomment%2F%7BentityType%7D%2F%7BentityId%7D/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `entityId` | path | `string` | yes |
| `entityType` | path | `string` | yes |
| `requestBody` | body | `object` | yes |
