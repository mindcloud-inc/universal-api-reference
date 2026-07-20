# Search People with DataForB2B

Searches for people in DataForB2B.

## Endpoint

- **Method:** `POST`
- **Path:** `/search/people`
- **Base URL:** `https://api.dataforb2b.ai`
- **Official documentation:** [Search People](https://docs.dataforb2b.ai/api-reference/search-people)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filters` | body | `object` | no | JSON filter object using DataForB2B search conditions. |
| `count` | body | `number` | no | Maximum number of results to return. |
| `offset` | body | `number` | no | Result offset for pagination. |
