# List Forms with Formcrafts

Retrieves a list of forms from Formcrafts.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms`
- **Base URL:** `https://api.formcrafts.com/v2`
- **Official documentation:** [List Forms](https://formcrafts.com/help/developers/api-docs-v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `before` | query | `string` | no | Return records created before this timestamp or resource marker, as supported by Formcrafts. |
| `after` | query | `string` | no | Return records created after this timestamp or resource marker, as supported by Formcrafts. |
