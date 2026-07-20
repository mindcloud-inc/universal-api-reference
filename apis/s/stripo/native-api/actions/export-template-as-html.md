# Export Template as HTML with Stripo

Exports a template as an HTML file from Stripo.

## Endpoint

- **Method:** `GET`
- **Path:** `/export/html/templates/:id`
- **Base URL:** `https://my.stripo.email/emailgeneration/v1`
- **Official documentation:** [Export Template as HTML](https://api.stripo.email/reference/exporttemplatetohtmlfile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asAmp` | query | `boolean` | no | Return AMPHTML code. |
| `id` | path | `number` | yes | The template ID. |
| `includeTranslationVersions` | query | `boolean` | no | Include translated versions in the export. |
| `minimize` | query | `boolean` | no | Compress the template output. |
| `setImageSizes` | query | `boolean` | no | Enable bidimensional image sizes. |
