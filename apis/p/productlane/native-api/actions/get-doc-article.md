# Get Doc Article with Productlane

Retrieves a help center article from Productlane.

## Endpoint

- **Method:** `GET`
- **Path:** `/docs/articles/{workspaceId}/{articleId}`
- **Base URL:** `https://productlane.com/api/v1`
- **Official documentation:** [Get Doc Article](https://productlane.mintlify.dev/docs/api/docs/get-doc-article)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | Workspace ID for the published docs site. |
| `articleId` | path | `string` | yes | Doc article ID. |
| `language` | query | `string` | no | Optional language override. |
