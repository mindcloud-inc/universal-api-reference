# Enrich Person with Hunter

## Endpoint

- **Method:** `GET`
- **Path:** `/people/find`
- **Base URL:** `https://api.hunter.io/v2`
- **Official documentation:** [Enrich Person](https://hunter.io/api-documentation/v2#email-enrichment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | Email address to enrich. |
| `linkedin_handle` | query | `string` | no | — |
| `clearbit_format` | query | `boolean` | no | — |
