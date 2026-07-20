# List Issues with Linear

Search Linear Issues.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://api.linear.app/graphql/`
- **API:** REST
- **Official documentation:** [List Issues](https://linear.app/developers/graphql#queries-and-mutations)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team` | body | `list` | no | — |
| `title` | body | `string` | no | — |
| `stateName` | body | `string` | no | — |
| `createdAfter` | body | `date` | no | Filter issues to return only those created after a specific date. |
| `updatedAfter` | body | `date` | no | — |
| `project` | body | `string` | no | The project that this issue is a part of. |
| `projectState` | body | `string` | no | The status of the Project this Issue is a part of. |
| `titleContains` | body | `string` | no | — |
