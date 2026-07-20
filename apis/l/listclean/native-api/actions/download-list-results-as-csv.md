# Download List Results As CSV with Listclean

Retrieves verification list results as a CSV file from Listclean.

## Endpoint

- **Method:** `GET`
- **Path:** `/downloads/:list_id/:type`
- **Base URL:** `https://api.listclean.xyz/v1`
- **Official documentation:** [Download List Results As CSV](https://api.listclean.xyz/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | path | `number` | yes | List ID whose results should be downloaded. |
| `type` | path | `list` | yes | Result type to download: clean, dirty, or unknown. Accepted values: `0`, `1`, `2`. |
