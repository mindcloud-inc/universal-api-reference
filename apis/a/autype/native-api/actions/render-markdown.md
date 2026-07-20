# Render Markdown with Autype

Creates a temporary document render job from markdown in Autype.

## Endpoint

- **Method:** `POST`
- **Path:** `/render/markdown`
- **Base URL:** `https://api.autype.com/api/v1/dev`
- **Official documentation:** [Render Markdown](https://docs.autype.com/api-reference/developer-api/render-markdown)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `content` | body | `string` | yes |
| `document` | body | `object` | yes |
| `strict` | query | `boolean` | no |
