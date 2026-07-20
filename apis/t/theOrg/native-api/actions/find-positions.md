# Find Positions with The Org

Finds positions in The Org by search filters.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.1/positions`
- **Base URL:** `https://api.theorg.com`
- **Official documentation:** [Find Positions](https://developers.theorg.com/api/endpoints/position-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | body | `number` | yes | Maximum number of results to return, up to 1000. |
| `offset` | body | `number` | yes | Result offset, up to 10000. |
| `filters` | body | `object` | yes | Search filters object matching the official Position API contract. |
