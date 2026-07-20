# Create Envelope from Template with Sign.Plus

## Endpoint

- **Method:** `POST`
- **Path:** `/envelope/from_template/:template_id`
- **Base URL:** `https://restapi.sign.plus/v2`
- **Official documentation:** [Create Envelope from Template](https://apidoc.sign.plus/api-reference/endpoints/signplus/create-new-envelope-from-template)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `template_id` | path | `string` | yes |
| `name` | body | `string` | yes |
| `comment` | body | `string` | no |
