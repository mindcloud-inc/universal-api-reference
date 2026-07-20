# Update Upload with DatoCMS

## Endpoint

- **Method:** `PUT`
- **Path:** `/uploads/:uploadId`
- **Base URL:** `https://site-api.datocms.com`
- **Official documentation:** [Update Upload](https://www.datocms.com/docs/content-management-api/resources/upload/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uploadId` | path | `string` | yes | Upload ID. |
| `data.attributes` | body | `object` | yes | Upload attributes payload. |
| `data.attributes.tags[]` | body | `array<string>` | no | — |
| `data.attributes.author` | body | `string` | no | — |
| `data.attributes.basename` | body | `string` | no | — |
| `data.attributes.copyright` | body | `string` | no | — |
| `data.attributes.notes` | body | `string` | no | — |
| `data.attributes.path` | body | `string` | no | — |
| `data.attributes.default_field_metadata` | body | `object` | no | — |
| `data.attributes.default_field_metadata.en` | body | `object` | no | — |
