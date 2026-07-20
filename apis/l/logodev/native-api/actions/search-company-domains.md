# Search Company Domains with Logo.dev

Finds company domains in Logo.dev.

## Endpoint

- **Method:** `GET`
- **Path:** `/search`
- **Base URL:** `https://api.logo.dev`
- **Official documentation:** [Search Company Domains](https://www.logo.dev/docs/brand-search/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Brand name query. |
| `strategy` | query | `string` | no | Search strategy: typeahead or match. |
