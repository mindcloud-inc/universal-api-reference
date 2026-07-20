# Create Upload with DatoCMS

## Endpoint

- **Method:** `POST`
- **Path:** `/uploads`
- **Base URL:** `https://site-api.datocms.com`
- **Official documentation:** [Create Upload](https://www.datocms.com/docs/content-management-api/resources/upload/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.attributes` | body | `object` | yes | Upload attributes payload. |
| `data.attributes.author` | body | `string` | no | — |
| `data.attributes.copyright` | body | `string` | no | — |
| `data.attributes.default_field_metadata` | body | `object` | no | — |
| `data.attributes.notes` | body | `string` | no | — |
| `data.attributes.path` | body | `string` | no | — |
| `data.attributes.tags[]` | body | `array<string>` | no | — |
| `data.attributes.default_field_metadata.en` | body | `object` | no | — |
