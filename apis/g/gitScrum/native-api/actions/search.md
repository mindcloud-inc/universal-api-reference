# Search with GitScrum

Finds matching records in GitScrum by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/search`
- **Base URL:** `https://services.gitscrum.com`
- **Official documentation:** [Search](https://docs.gitscrum.com/en/api/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_slug` | query | `string` | no | — |
| `q` | query | `string` | no | Text to search for across the workspace. |
