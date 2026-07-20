# Create Change Request with GitBook

Creates a new change request in GitBook.

## Endpoint

- **Method:** `POST`
- **Path:** `/spaces/:spaceId/change-requests`
- **Base URL:** `https://api.gitbook.com/v1`
- **Official documentation:** [Create Change Request](https://gitbook.com/docs/developers/gitbook-api/api-reference/change-requests)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `spaceId` | path | `string` | yes |
| `subject` | body | `string` | no |
