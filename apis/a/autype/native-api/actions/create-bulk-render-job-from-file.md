# Create Bulk Render Job From File with Autype

Creates a bulk render job from a file in Autype.

## Endpoint

- **Method:** `POST`
- **Path:** `/bulk-render/file`
- **Base URL:** `https://api.autype.com/api/v1/dev`
- **Official documentation:** [Create Bulk Render Job From File](https://docs.autype.com/api-reference/developer-api/create-bulk-render-job-from-file)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `documentId` | body | `string` | yes |
| `file` | body | `file` | yes |
| `format` | body | `string` | yes |
