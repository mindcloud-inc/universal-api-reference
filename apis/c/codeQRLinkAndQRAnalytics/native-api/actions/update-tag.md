# Update Tag with CodeQR - Link and QR Analytics

Updates a tag in CodeQR.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tags/:id`
- **Base URL:** `https://api.codeqr.io`
- **Official documentation:** [Update Tag](https://app.stainless.com/api/spec/documented/codeqr/openapi.documented.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the tag to update. |
| `name` | body | `string` | yes | The name of the tag. |
| `color` | body | `string` | no | The color of the tag. |
