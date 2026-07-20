# Retrieve Records with Algolia

Retrieves records from one or more Algolia indices.

## Endpoint

- **Method:** `POST`
- **Path:** `/1/indexes/*/objects`
- **Base URL:** `https://{applicationId}.algolia.net`
- **Official documentation:** [Retrieve Records](https://www.algolia.com/doc/rest-api/search/get-objects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requests[]` | body | `array<object>` | yes | Record lookup requests across one or more indices. |
