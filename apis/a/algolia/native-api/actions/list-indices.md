# List Indices with Algolia

Retrieves all indices in the Algolia application.

## Endpoint

- **Method:** `GET`
- **Path:** `/1/indexes`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [List Indices](https://www.algolia.com/doc/rest-api/search/list-indices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page of indices to retrieve. |
| `hitsPerPage` | query | `number` | no | Maximum number of indices to return. |
