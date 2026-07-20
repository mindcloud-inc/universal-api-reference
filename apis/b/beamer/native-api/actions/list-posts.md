# List Posts with Beamer

Retrieves posts from Beamer.

## Endpoint

- **Method:** `GET`
- **Path:** `/v0/posts`
- **Base URL:** `https://api.getbeamer.com`
- **Official documentation:** [List Posts](https://help.userflow.com/beamer/docs/beamer-api-reference)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | Retrieve posts with a matching segmentation filter. |
| `forceFilter` | query | `string` | no | Only retrieve posts that match this segmentation filter. |
| `filterUrl` | query | `string` | no | Include posts with a matching segmentation URL. |
| `dateFrom` | query | `string` | no | Retrieve posts published after this ISO-8601 date. |
| `dateTo` | query | `string` | no | Retrieve posts published before this ISO-8601 date. |
| `language` | query | `string` | no | Retrieve posts with translations in this language. |
| `category` | query | `string` | no | Retrieve posts with this category. |
| `published` | query | `boolean` | no | Retrieve only published or draft posts. |
| `archived` | query | `boolean` | no | Retrieve only archived or non-archived posts. |
| `expired` | query | `boolean` | no | Retrieve only expired or non-expired posts. |
| `filterByUserId` | query | `boolean` | no | Retrieve posts filtered by user ID. |
| `userFirstName` | query | `string` | no | First name of the user viewing these posts. |
| `userLastName` | query | `string` | no | Last name of the user viewing these posts. |
| `userEmail` | query | `string` | no | Email of the user viewing these posts. |
| `userId` | query | `string` | no | ID of the user viewing these posts. |
| `traceableLinks` | query | `boolean` | no | Whether to include traceable links in posts. |
| `ignoreRequestDetails` | query | `boolean` | no | Ignore request details used for analytics. |
| `saveViews` | query | `boolean` | no | Whether to save views for the requesting user. |
| `ignoreFilters` | query | `boolean` | no | Ignore feed filters when retrieving posts. |
