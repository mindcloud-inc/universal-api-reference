# Create Tag with CodeQR - Link and QR Analytics

Creates a tag in CodeQR.

## Endpoint

- **Method:** `POST`
- **Path:** `/tags`
- **Base URL:** `https://api.codeqr.io`
- **Official documentation:** [Create Tag](https://app.stainless.com/api/spec/documented/codeqr/openapi.documented.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the tag to create. |
| `color` | body | `string` | no | The color of the tag. |
