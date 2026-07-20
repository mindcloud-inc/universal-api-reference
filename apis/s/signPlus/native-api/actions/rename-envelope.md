# Rename Envelope with Sign.Plus

## Endpoint

- **Method:** `PUT`
- **Path:** `/envelope/:envelope_id/rename`
- **Base URL:** `https://restapi.sign.plus/v2`
- **Official documentation:** [Rename Envelope](https://apidoc.sign.plus/api-reference/endpoints/signplus/rename-envelope)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `envelope_id` | path | `string` | yes |
| `name` | body | `string` | yes |
