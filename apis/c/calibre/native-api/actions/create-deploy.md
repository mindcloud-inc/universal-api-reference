# Create Deploy with Calibre

Creates a new deploy in Calibre.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.calibreapp.com`
- **Official documentation:** [Create Deploy](https://calibreapp.com/docs/automation/deploys#create-deploy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.site` | body | `string` | yes | Site slug, found in site settings. |
| `variables.revision` | body | `string` | no | Source control revision or tag name for the deploy. |
| `variables.repository` | body | `string` | no | Base URL of the repository containing the deployed code. |
| `variables.username` | body | `string` | no | Name of the user who deployed the code. |
| `variables.createdAt` | body | `string` | no | ISO8601 timestamp for when the deploy was created. |
