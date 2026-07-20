# List Document Templates with Feathery

## Endpoint

- **Method:** `GET`
- **Path:** `/api/document/template/`
- **Base URL:** `https://api.feathery.io`
- **Official documentation:** [List Document Templates](https://api-docs.feathery.io/#list-document-templates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Only return document templates whose names contain this value. |
| `tags` | query | `string` | no | Tag filter values. Feathery treats repeated `tags` query parameters as AND conditions and `;;` within one value as OR. Send multiple values as a array. |
