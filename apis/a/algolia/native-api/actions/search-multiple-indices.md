# Search Multiple Indices with Algolia

Searches multiple Algolia indices in one request.

## Endpoint

- **Method:** `POST`
- **Path:** `/1/indexes/*/queries`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Search Multiple Indices](https://www.algolia.com/doc/rest-api/search/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requests[]` | body | `array<object>` | yes | Search requests to run across one or more indices. |
| `strategy` | body | `list` | no | Whether to run all queries or stop after enough matches. Accepted values: `0`, `1`. |
