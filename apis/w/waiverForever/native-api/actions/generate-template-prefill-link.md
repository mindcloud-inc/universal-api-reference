# Generate Template Prefill Link with WaiverForever

Creates a prefilled template link in WaiverForever.

## Endpoint

- **Method:** `POST`
- **Path:** `/openapi/v2/template/:template_id/prefill`
- **Base URL:** `https://api.waiverforever.com`
- **Official documentation:** [Generate Template Prefill Link](https://docs.waiverforever.com/#generate-template-prefill-link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `expire_at` | body | `number` | no | Expiration timestamp for the generated prefill link. |
| `fields` | body | `object` | yes | Prefilled field values that must match the template prefill schema for the template. |
| `template_id` | path | `string` | yes | WaiverForever template identifier. |
