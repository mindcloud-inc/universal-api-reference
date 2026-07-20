# Fetch Prospects with Explorium

Fetches prospects from Explorium API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/prospects`
- **Base URL:** `https://api.explorium.ai`
- **Official documentation:** [Fetch Prospects](https://developers.explorium.ai/reference/prospects/fetch_prospects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mode` | body | `string` | yes | Response mode. Explorium requires `full` or `preview`. |
| `page_size` | body | `number` | yes | The number of results to return. |
