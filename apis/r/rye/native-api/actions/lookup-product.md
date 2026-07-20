# Lookup Product with Rye

Finds a product in Rye by URL.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/products/lookup`
- **Base URL:** `https://staging.api.rye.com`
- **Official documentation:** [Lookup Product](https://rye.com/docs/api-v2/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | The product URL to look up. |
