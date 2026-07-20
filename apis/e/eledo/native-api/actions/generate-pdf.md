# Generate PDF with Eledo

Generates a PDF from a template in Eledo.

## Endpoint

- **Method:** `POST`
- **Path:** `/Generate`
- **Base URL:** `https://eledo.online/api/RESTv1`
- **Official documentation:** [Generate PDF](https://eledo.online/documentation/api_reference/generate)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `templateId` | body | `string` | yes |
| `templateVersion` | body | `number` | no |
| `file` | body | `object` | no |
