# Search Resources with Acronis

Finds resources in Acronis by search expression.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/resource_management/v4/resources`
- **Base URL:** `{dataCenterUrl}`
- **Official documentation:** [Search Resources](https://developer.acronis.com/doc/outbound/apis/api-library/resource-policy/resources/fetching-resources-using-search.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | yes | Acronis resource search expression. |
