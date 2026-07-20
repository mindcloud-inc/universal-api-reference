# Update Visitor with condoo

Updates an existing visitor in condoo.

## Endpoint

- **Method:** `POST`
- **Path:** `/visitors/{visitor_id}`
- **Base URL:** `https://trk.condoo.systems/api`
- **Official documentation:** [Update Visitor](https://trk.condoo.systems/en/api-documentation/visitors)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `custom_parameter_key[0]` | body | `string` | no | Optional first custom parameter key. |
| `custom_parameter_value[0]` | body | `string` | no | Optional first custom parameter value. |
| `visitor_id` | path | `string` | yes | Required visitor ID or visitor UUID. |
