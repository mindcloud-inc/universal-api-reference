# Query Multiple Jobs with Avionte

## Endpoint

- **Method:** `POST`
- **Path:** `front-office/v1/jobs/multi-query`
- **Base URL:** `https://api.avionte.com/`
- **Official documentation:** [Query Multiple Jobs](https://developer.avionte.com/reference/querymultiplejobs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `jobIds` | body | `string` | yes |
