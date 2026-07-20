# List Authors with Moderation API

Retrieves authors from Moderation API.

## Endpoint

- **Method:** `GET`
- **Path:** `/authors`
- **Base URL:** `https://api.moderationapi.com/v1`
- **Official documentation:** [List Authors](https://docs.moderationapi.com/api-reference/author/list-authors)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageSize` | query | `number` | no | Number of authors per page |
| `pageNumber` | query | `number` | no | Page number to fetch |
| `sortBy` | query | `string` | no | — |
| `sortDirection` | query | `string` | no | Sort direction |
| `memberSinceDate` | query | `string` | no | — |
| `lastActiveDate` | query | `string` | no | — |
| `contentTypes` | query | `string` | no | — |
