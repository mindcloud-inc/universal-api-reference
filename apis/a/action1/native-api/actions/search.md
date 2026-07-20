# Search with Action1

Finds Action1 objects in an organization by query.

## Endpoint

- **Method:** `GET`
- **Path:** `/search/:orgId`
- **Base URL:** `https://app.action1.com/api/3.0`
- **Official documentation:** [Search](https://app.action1.com/apidocs/#/Search/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orgId` | path | `string` | yes | Provide an organization ID. Most API calls are scoped to one organization. |
| `query` | query | `string` | yes | Provide a query for searching. |
