# Download List Results As JSON with Listclean

Retrieves verification list results as JSON from Listclean.

## Endpoint

- **Method:** `GET`
- **Path:** `/downloads/json/:list_id/:type`
- **Base URL:** `https://api.listclean.xyz/v1`
- **Official documentation:** [Download List Results As JSON](https://api.listclean.xyz/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | path | `number` | yes | List ID whose results should be downloaded. |
| `type` | path | `list` | yes | Result type to download: clean, dirty, or unknown. Accepted values: `0`, `1`, `2`. |
