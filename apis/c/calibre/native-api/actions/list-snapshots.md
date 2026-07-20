# List Snapshots with Calibre

Retrieves snapshots for a site from Calibre.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.calibreapp.com`
- **Official documentation:** [List Snapshots](https://calibreapp.com/docs/automation/snapshots#list-snapshots)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.site` | body | `string` | yes | Site slug, found in site settings. |
| `variables.first` | body | `number` | no | Maximum number of snapshots to return. |
