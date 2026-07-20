# Update Project with Documently

Updates an existing project in Documently.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:projectId`
- **Base URL:** `https://app.documently.io/api`
- **Official documentation:** [Update Project](https://app.documently.io/api/docs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/ld+json` |
| `Content-Type` | `application/merge-patch+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `defaultLanguage` | body | `string` | no | Default project language. |
| `name` | body | `string` | no | Project name. |
| `projectId` | path | `string` | no | The project id. |
| `publicUrl` | body | `boolean` | no | Whether the project has a public URL. |
