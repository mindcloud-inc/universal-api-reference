# Search Records with Attio

Finds records in Attio by fuzzy search.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/objects/records/search`
- **Base URL:** `https://api.attio.com`
- **Official documentation:** [Search Records](https://docs.attio.com/rest-api/endpoint-reference/records/search-records)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | Query string to search for. An empty string returns a default set of results. |
| `objects[]` | body | `array<string>` | yes | One or more Attio object slugs or UUIDs to search within. |
| `limit` | body | `number` | no | Maximum number of results to return. |
