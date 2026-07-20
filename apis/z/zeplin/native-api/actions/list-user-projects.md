# List User Projects with Zeplin

Retrieves a list of user projects from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/me/projects`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List User Projects](https://docs.zeplin.dev/reference/getuserprojects)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Filter by status |
