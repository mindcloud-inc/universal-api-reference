# List Change Requests with GitBook

Retrieves change requests from a GitBook space.

## Endpoint

- **Method:** `GET`
- **Path:** `/spaces/:spaceId/change-requests`
- **Base URL:** `https://api.gitbook.com/v1`
- **Official documentation:** [List Change Requests](https://gitbook.com/docs/developers/gitbook-api/api-reference/change-requests)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contributor` | query | `string` | no |
| `creator` | query | `string` | no |
| `orderBy` | query | `string` | no |
| `requestedReviewer` | query | `string` | no |
| `spaceId` | path | `string` | yes |
| `status` | query | `string` | no |
| `topic` | query | `string` | no |
