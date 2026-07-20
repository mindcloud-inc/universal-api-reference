# Search Annotations with Rossum

Finds annotations in Rossum using a complex filter.

## Endpoint

- **Method:** `POST`
- **Path:** `/annotations/search`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Search Annotations](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query_string.string` | body | `string` | yes | Full-text search term (minimum 2 characters). |
| `page_size` | query | `number` | no | Number of results per page (max 500). |
