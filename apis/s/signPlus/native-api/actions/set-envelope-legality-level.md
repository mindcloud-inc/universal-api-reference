# Set Envelope Legality Level with Sign.Plus

## Endpoint

- **Method:** `PUT`
- **Path:** `/envelope/:envelope_id/set_legality_level`
- **Base URL:** `https://restapi.sign.plus/v2`
- **Official documentation:** [Set Envelope Legality Level](https://apidoc.sign.plus/api-reference/endpoints/signplus/set-envelope-legality-level)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `envelope_id` | path | `string` | yes |
| `legality_level` | body | `string` | yes |
