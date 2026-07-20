# Batch Lite IP Lookups with IPInfo

## Endpoint

- **Method:** `POST`
- **Path:** `/batch/lite`
- **Base URL:** `https://api.ipinfo.io`
- **Official documentation:** [Batch Lite IP Lookups](https://ipinfo.io/developers/advanced-usage)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requests` | body | `string` | yes | JSON array of IPs or URL patterns to enrich in the Lite batch endpoint. |
