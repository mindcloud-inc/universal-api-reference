# Update Talent with Avionte

## Endpoint

- **Method:** `PUT`
- **Path:** `front-office/v1/talent/:talentId`
- **Base URL:** `https://api.avionte.com/`
- **Official documentation:** [Update Talent](https://developer.avionte.com/reference/updatetalent)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `talentId` | path | `string` | no |
| `talent` | body | `string` | yes |
