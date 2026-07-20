# List referring IPs with SE Ranking Data

Retrieves referring IPs from SE Ranking Data.

## Endpoint

- **Method:** `GET`
- **Path:** `/backlinks/referring-ips`
- **Base URL:** `https://api.seranking.com/v1`
- **Official documentation:** [List referring IPs](https://seranking.com/api/data/backlinks/#referring-ips)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target` | query | `string` | yes | Target domain or URL to analyze (for example: seranking.com). |
