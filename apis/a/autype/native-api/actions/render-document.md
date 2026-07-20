# Render Document with Autype

Creates a temporary document render job from JSON in Autype.

## Endpoint

- **Method:** `POST`
- **Path:** `/render`
- **Base URL:** `https://api.autype.com/api/v1/dev`
- **Official documentation:** [Render Document](https://docs.autype.com/api-reference/developer-api/render-document)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `config` | body | `object` | yes |
| `strict` | query | `boolean` | no |
| `webhook` | body | `object` | no |
