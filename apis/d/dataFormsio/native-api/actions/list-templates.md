# List Templates with DataForms.io

Retrieves templates from DataForms.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/templates`
- **Base URL:** `https://api.dataforms.io`
- **Official documentation:** [List Templates](https://dataforms.readme.io/reference/index-templates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Filter templates by search term. |
| `limit` | query | `number` | no | Limit the number of templates returned. Maximum 50. |
