# Create a new project with Xata

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations/:organizationID/projects`
- **Base URL:** `https://api.xata.tech`
- **Official documentation:** [Create a new project](https://xata.io/docs/api-reference/projects/create-a-new-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationID` | path | `string` | yes | Unique identifier of the organization to create the project in |
| `name` | body | `string` | yes | Human-readable name for the new project |
| `configuration` | body | `object` | no | — |
