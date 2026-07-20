# Update Goal Conversion with condoo

Updates an existing goal conversion in condoo.

## Endpoint

- **Method:** `POST`
- **Path:** `/goals-conversions/{conversion_id}`
- **Base URL:** `https://trk.condoo.systems/api`
- **Official documentation:** [Update Goal Conversion](https://trk.condoo.systems/en/api-documentation/goals-conversions)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversion_id` | path | `number` | yes | Required goal conversion ID. |
| `key` | body | `string` | no | Documented update field; provider docs may be inconsistent for conversion updates. |
| `name` | body | `string` | no | Documented update field; provider docs may be inconsistent for conversion updates. |
| `path` | body | `string` | no | Documented update field; provider docs may be inconsistent for conversion updates. |
| `type` | body | `string` | no | Documented update field; provider docs may be inconsistent for conversion updates. |
| `website_id` | body | `number` | no | Documented update field; provider docs may be inconsistent for conversion updates. |
