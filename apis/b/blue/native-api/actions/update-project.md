# Update Project with Blue

Updates an existing project in Blue.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.blue.cc`
- **Official documentation:** [Update Project](https://blue.cc/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.projectId` | body | `string` | yes | Blue project node ID. |
| `variables.name` | body | `string` | no | Updated project name. |
| `variables.description` | body | `string` | no | Updated project description. |
