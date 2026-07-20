# Get Auth Token (Email and Password) with Onethread

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/login`
- **Base URL:** `https://api.onethread.app/api/v1`
- **Official documentation:** [Get Auth Token (Email and Password)](https://docs.onethreadapp.com/3.-getting-started/3.2-log-in)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | body | `string` | no |
| `password` | body | `string` | no |
