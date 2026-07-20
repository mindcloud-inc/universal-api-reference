# Get Scrape Status with Scrapi

Retrieves a Scrapi scrape status by callback reference.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/scrape/status/{reference}`
- **Base URL:** `https://api.scrapi.tech`
- **Official documentation:** [Get Scrape Status](https://scrapi.tech/docs/api_details/v1_scrape)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reference` | path | `string` | yes | Callback reference to inspect. |
