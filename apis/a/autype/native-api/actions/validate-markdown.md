# Validate Markdown with Autype

Validates document markdown content in Autype.

## Endpoint

- **Method:** `POST`
- **Path:** `/render/validate/markdown`
- **Base URL:** `https://api.autype.com/api/v1/dev`
- **Official documentation:** [Validate Markdown](https://docs.autype.com/api-reference/developer-api/validate-markdown)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `content` | body | `string` | yes |
| `document` | body | `object` | yes |
