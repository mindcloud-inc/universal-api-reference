# Set Envelope Dynamic Fields with Sign.Plus

## Endpoint

- **Method:** `PUT`
- **Path:** `/envelope/:envelope_id/dynamic_fields`
- **Base URL:** `https://restapi.sign.plus/v2`
- **Official documentation:** [Set Envelope Dynamic Fields](https://apidoc.sign.plus/api-reference/endpoints/signplus/set-envelope-dynamic-fields)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `envelope_id` | path | `string` | yes |
| `dynamic_fields[]` | body | `array<object>` | yes |
