# Learn New IP with Control D

Creates a known IP in Control D.

## Endpoint

- **Method:** `POST`
- **Path:** `/access`
- **Base URL:** `https://api.controld.com`
- **Official documentation:** [Learn New IP](https://docs.controld.com/reference/post_access)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `device_id` | body | `string` | yes | Primary key of the device. |
| `ips[]` | body | `array<string>` | yes | IPv4 or IPv6 addresses |
