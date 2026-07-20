# List Docs with Dart

Retrieves docs from Dart with optional title filtering.

## Endpoint

- **Method:** `GET`
- **Path:** `/docs/list`
- **Base URL:** `https://app.dartai.com/api/v0/public`
- **Official documentation:** [List Docs](https://app.dartai.com/api/v0/public/docs/#/Doc/listDocs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `limit` | query | `string` | no |
| `offset` | query | `string` | no |
| `title` | query | `string` | no |
