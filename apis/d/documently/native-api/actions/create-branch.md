# Create Branch with Documently

Creates a new branch in Documently.

## Endpoint

- **Method:** `POST`
- **Path:** `/branches`
- **Base URL:** `https://app.documently.io/api`
- **Official documentation:** [Create Branch](https://app.documently.io/api/docs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/ld+json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `project` | body | `string` | yes |
| `status` | body | `string` | yes |
