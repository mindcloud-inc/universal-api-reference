# Promote Custom Fields to Experience Fields with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/experience-fields`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Promote Custom Fields to Experience Fields](https://developers.gobridgit.com/reference/experiencefields_promotecustomfields)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | path | `number` | yes |
| `payload[]` | body | `array<number>` | yes |
