# Update Issue with Linear

Update Linear Issue.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://api.linear.app/graphql/`
- **API:** REST
- **Official documentation:** [Update Issue](https://linear.app/developers/graphql#queries-and-mutations)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | body | `string` | yes |
| `team` | body | `list` | no |
| `title` | body | `string` | no |
| `description` | body | `string` | no |
