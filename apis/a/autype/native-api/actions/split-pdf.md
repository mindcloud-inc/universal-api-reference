# Split PDF with Autype

Creates a PDF split job in Autype.

## Endpoint

- **Method:** `POST`
- **Path:** `/tools/pdf/split`
- **Base URL:** `https://api.autype.com/api/v1/dev`
- **Official documentation:** [Split PDF](https://docs.autype.com/api-reference/developer-api/split-pdf)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `fileId` | body | `string` | yes |
| `ranges[]` | body | `array<string>` | yes |
