# List Workspaces with Formcrafts

Retrieves a list of workspaces from Formcrafts.

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces`
- **Base URL:** `https://api.formcrafts.com/v2`
- **Official documentation:** [List Workspaces](https://formcrafts.com/help/developers/api-docs-v2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `before` | query | `string` | no | Return records created before this timestamp or resource marker, as supported by Formcrafts. |
| `after` | query | `string` | no | Return records created after this timestamp or resource marker, as supported by Formcrafts. |
