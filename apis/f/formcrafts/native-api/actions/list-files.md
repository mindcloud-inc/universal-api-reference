# List Files with Formcrafts

Retrieves a list of uploaded files from Formcrafts.

## Endpoint

- **Method:** `GET`
- **Path:** `/files`
- **Base URL:** `https://api.formcrafts.com/v2`
- **Official documentation:** [List Files](https://formcrafts.com/help/developers/api-docs-v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `before` | query | `string` | no | Return records created before this timestamp or resource marker, as supported by Formcrafts. |
| `after` | query | `string` | no | Return records created after this timestamp or resource marker, as supported by Formcrafts. |
