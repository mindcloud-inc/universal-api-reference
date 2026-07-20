# List Deploys with Calibre

Retrieves deploys for a site from Calibre.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.calibreapp.com`
- **Official documentation:** [List Deploys](https://calibreapp.com/docs/automation/deploys#list-deploys)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.site` | body | `string` | yes | Site slug, found in site settings. |
| `variables.first` | body | `number` | no | Maximum number of deploys to return. |
| `variables.from` | body | `string` | no | Lower bound ISO8601 date filter for deploys. |
| `variables.to` | body | `string` | no | Upper bound ISO8601 date filter for deploys. |
