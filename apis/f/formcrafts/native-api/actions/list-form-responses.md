# List Form Responses with Formcrafts

Retrieves responses for a form from Formcrafts.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:id/responses`
- **Base URL:** `https://api.formcrafts.com/v2`
- **Official documentation:** [List Form Responses](https://formcrafts.com/help/developers/api-docs-v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Formcrafts form ID. |
| `before` | query | `string` | no | Return records created before this timestamp or resource marker, as supported by Formcrafts. |
| `after` | query | `string` | no | Return records created after this timestamp or resource marker, as supported by Formcrafts. |
