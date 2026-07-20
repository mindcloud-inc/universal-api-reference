# Add Envelope Signing Steps with Sign.Plus

## Endpoint

- **Method:** `POST`
- **Path:** `/envelope/:envelope_id/signing_steps`
- **Base URL:** `https://restapi.sign.plus/v2`
- **Official documentation:** [Add Envelope Signing Steps](https://apidoc.sign.plus/api-reference/endpoints/signplus/add-envelope-signing-steps)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `envelope_id` | path | `string` | yes |
| `signing_steps[]` | body | `array<object>` | yes |
