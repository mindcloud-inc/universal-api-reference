# List User Projects with Mendix

Retrieves a user's project memberships from Mendix.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:userId/projects`
- **Base URL:** `https://projects-api.home.mendix.com/v2`
- **API:** rest
- **Official documentation:** [List User Projects](https://docs.mendix.com/apidocs-mxsdk/apidocs/projects-api/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user-id` | path | `string` | yes | The unique identifier of a user. |
| `permissions` | query | `string` | no | Comma-separated permissions to filter by, such as administrator, technicalcontact, repositoryaccess, cloudportalaccess, or teamserveraccess. |
| `isPinnedByUser` | query | `boolean` | no | Whether the user has pinned the project as a favorite. If omitted, both pinned and unpinned projects are returned. |
| `categories` | query | `string` | no | Comma-separated categories with values in the documented Mendix filter format. |
