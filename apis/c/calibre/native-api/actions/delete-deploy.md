# Delete Deploy with Calibre

Deletes an existing deploy from Calibre.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.calibreapp.com`
- **Official documentation:** [Delete Deploy](https://calibreapp.com/docs/automation/deploys#delete-deploy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.site` | body | `string` | yes | Site slug, found in site settings. |
| `variables.uuid` | body | `string` | yes | UUID of the deploy to delete. |
