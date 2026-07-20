# Set Envelope Comment with Sign.Plus

## Endpoint

- **Method:** `PUT`
- **Path:** `/envelope/:envelope_id/set_comment`
- **Base URL:** `https://restapi.sign.plus/v2`
- **Official documentation:** [Set Envelope Comment](https://apidoc.sign.plus/api-reference/endpoints/signplus/set-envelope-comment)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `envelope_id` | path | `string` | yes |
| `comment` | body | `string` | yes |
