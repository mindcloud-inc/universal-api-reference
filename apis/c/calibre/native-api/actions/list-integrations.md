# List Integrations with Calibre

Retrieves integrations for a site from Calibre.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.calibreapp.com`
- **Official documentation:** [List Integrations](https://calibreapp.com/docs/automation/integrations#list-integrations)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `variables.site` | body | `string` | yes |
| `variables.first` | body | `number` | no |
