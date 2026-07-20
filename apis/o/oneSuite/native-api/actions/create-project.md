# Create Project with OneSuite

Creates a project in OneSuite.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/projects`
- **Base URL:** `https://api.onesuite.io`
- **Official documentation:** [Create Project](https://rest-api.onesuite.io/#create-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the project |
| `status.key` | body | `string` | no | Project status key |
| `client.key` | body | `string` | no | Client ID for the project |
| `privacy` | body | `list` | no | Project privacy Accepted values: `0`, `1`. |
