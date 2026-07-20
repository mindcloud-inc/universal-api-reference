# Get Crawler Attributes with LOBSTR.IO

Retrieves crawler attributes from LOBSTR.IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/crawlers/:crawler_hash/attributes`
- **Base URL:** `https://api.lobstr.io`
- **Official documentation:** [Get Crawler Attributes](https://docs.lobstr.io/docs/get-crawler-attributes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `crawler_hash` | path | `string` | yes | The unique identifier (hash) of the crawler. |
