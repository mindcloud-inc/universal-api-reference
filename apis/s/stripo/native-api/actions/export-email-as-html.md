# Export Email as HTML with Stripo

Exports an email as an HTML file from Stripo.

## Endpoint

- **Method:** `GET`
- **Path:** `/export/html/emails/:id`
- **Base URL:** `https://my.stripo.email/emailgeneration/v1`
- **Official documentation:** [Export Email as HTML](https://api.stripo.email/reference/exportemailtohtmlfile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asAmp` | query | `boolean` | no | Return AMPHTML code. |
| `id` | path | `number` | yes | The email ID. |
| `includeTranslationVersions` | query | `boolean` | no | Include translated versions in the export. |
| `minimize` | query | `boolean` | no | Compress the email output. |
| `setImageSizes` | query | `boolean` | no | Enable bidimensional image sizes. |
