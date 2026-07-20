# List Unread Posts with Beamer

Retrieves unread posts from Beamer.

## Endpoint

- **Method:** `GET`
- **Path:** `/v0/unread`
- **Base URL:** `https://api.getbeamer.com`
- **Official documentation:** [List Unread Posts](https://help.userflow.com/beamer/docs/beamer-api-reference)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `filter` | query | `string` | no |
| `forceFilter` | query | `string` | no |
| `filterUrl` | query | `string` | no |
| `dateFrom` | query | `string` | no |
| `language` | query | `string` | no |
| `category` | query | `string` | no |
| `userFirstName` | query | `string` | no |
| `userLastName` | query | `string` | no |
| `userEmail` | query | `string` | no |
| `userId` | query | `string` | no |
| `traceableLinks` | query | `boolean` | no |
| `ignoreRequestDetails` | query | `boolean` | no |
| `saveViews` | query | `boolean` | no |
| `markAsRead` | query | `boolean` | no |
| `ignoreFilters` | query | `boolean` | no |
