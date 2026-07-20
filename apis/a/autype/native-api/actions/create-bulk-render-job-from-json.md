# Create Bulk Render Job From JSON with Autype

Creates a bulk render job from JSON in Autype.

## Endpoint

- **Method:** `POST`
- **Path:** `/bulk-render`
- **Base URL:** `https://api.autype.com/api/v1/dev`
- **Official documentation:** [Create Bulk Render Job From JSON](https://docs.autype.com/api-reference/developer-api/create-bulk-render-job-from-json)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `documentId` | body | `string` | yes |
| `format` | body | `string` | yes |
| `items[]` | body | `array<object>` | yes |
