# Estimate Position Search Credit Usage with The Org

Estimates position search credit usage in The Org.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.1/positions/credit-usage`
- **Base URL:** `https://api.theorg.com`
- **Official documentation:** [Estimate Position Search Credit Usage](https://developers.theorg.com/api/endpoints/position-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | body | `number` | yes | Maximum number of results to return, up to 1000. |
| `offset` | body | `number` | yes | Result offset, up to 10000. |
| `filters` | body | `object` | yes | Search filters object matching the official Position API contract. |
