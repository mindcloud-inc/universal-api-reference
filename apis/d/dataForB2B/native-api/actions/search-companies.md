# Search Companies with DataForB2B

Searches for companies in DataForB2B.

## Endpoint

- **Method:** `POST`
- **Path:** `/search/companies`
- **Base URL:** `https://api.dataforb2b.ai`
- **Official documentation:** [Search Companies](https://docs.dataforb2b.ai/api-reference/search-company)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | body | `object` | no | JSON filter object using company search conditions. |
| `count` | body | `number` | no | Maximum number of results to return. |
| `offset` | body | `number` | no | Result offset for pagination. |
