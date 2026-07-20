# Count Posts with Beamer

Retrieves a post count from Beamer.

## Endpoint

- **Method:** `GET`
- **Path:** `/v0/posts/count`
- **Base URL:** `https://api.getbeamer.com`
- **Official documentation:** [Count Posts](https://help.userflow.com/beamer/docs/beamer-api-reference)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `filter` | query | `string` | no |
| `forceFilter` | query | `string` | no |
| `filterUrl` | query | `string` | no |
| `dateFrom` | query | `string` | no |
| `dateTo` | query | `string` | no |
| `language` | query | `string` | no |
| `category` | query | `string` | no |
| `published` | query | `boolean` | no |
| `archived` | query | `boolean` | no |
| `expired` | query | `boolean` | no |
| `filterByUserId` | query | `boolean` | no |
| `userId` | query | `string` | no |
| `ignoreFilters` | query | `boolean` | no |
