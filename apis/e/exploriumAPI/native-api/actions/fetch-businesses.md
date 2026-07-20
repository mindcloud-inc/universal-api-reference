# Fetch Businesses with Explorium

Fetches businesses from Explorium API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/businesses`
- **Base URL:** `https://api.explorium.ai`
- **Official documentation:** [Fetch Businesses](https://developers.explorium.ai/reference/businesses/fetch_businesses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mode` | body | `string` | yes | Response mode. Explorium requires `full` or `preview`. |
| `page_size` | body | `number` | yes | The number of results to return. |
