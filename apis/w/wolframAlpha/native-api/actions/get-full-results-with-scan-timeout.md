# Get Full Results with Scan Timeout with Wolfram Alpha

Retrieves full Wolfram Alpha query results with a scan timeout.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/query`
- **Base URL:** `https://api.wolframalpha.com`
- **Official documentation:** [Get Full Results with Scan Timeout](https://products.wolframalpha.com/api/documentation)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `input` | query | `string` | yes |
| `scantimeout` | query | `number` | yes |
