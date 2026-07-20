# Rotate PDF Pages with Autype

Creates a PDF rotation job in Autype.

## Endpoint

- **Method:** `POST`
- **Path:** `/tools/pdf/rotate`
- **Base URL:** `https://api.autype.com/api/v1/dev`
- **Official documentation:** [Rotate PDF Pages](https://docs.autype.com/api-reference/developer-api/rotate-pdf-pages)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `angle` | body | `number` | yes |
| `fileId` | body | `string` | yes |
| `pages[]` | body | `array<string>` | yes |
