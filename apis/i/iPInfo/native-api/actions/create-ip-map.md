# Create IP Map with IPInfo

## Endpoint

- **Method:** `POST`
- **Path:** `/tools/map`
- **Base URL:** `https://api.ipinfo.io`
- **Official documentation:** [Create IP Map](https://ipinfo.io/tools/map)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/plain` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ipAddresses` | body | `string` | yes | Newline-delimited list of IP addresses to place on a map. |
