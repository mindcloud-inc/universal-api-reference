# Set Envelope Expiration Date with Sign.Plus

## Endpoint

- **Method:** `PUT`
- **Path:** `/envelope/:envelope_id/set_expiration_date`
- **Base URL:** `https://restapi.sign.plus/v2`
- **Official documentation:** [Set Envelope Expiration Date](https://apidoc.sign.plus/api-reference/endpoints/signplus/set-envelope-expiration-date)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `envelope_id` | path | `string` | yes |
| `expires_at` | body | `number` | yes |
