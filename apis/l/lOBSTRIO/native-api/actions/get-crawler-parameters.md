# Get Crawler Parameters with LOBSTR.IO

Retrieves crawler parameters from LOBSTR.IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/crawlers/:crawler_hash/params`
- **Base URL:** `https://api.lobstr.io`
- **Official documentation:** [Get Crawler Parameters](https://docs.lobstr.io/docs/get-crawler-parameters)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `crawler_hash` | path | `string` | yes | The unique identifier (hash) of the crawler. |
