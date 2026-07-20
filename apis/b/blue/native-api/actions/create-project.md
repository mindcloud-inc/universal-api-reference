# Create Project with Blue

Creates a new project in Blue.

## Endpoint

- **Method:** `POST`
- **Path:** `/graphql`
- **Base URL:** `https://api.blue.cc`
- **Official documentation:** [Create Project](https://blue.cc/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.companyId` | body | `string` | yes | Blue company node ID. |
| `variables.name` | body | `string` | yes | Project name. |
| `variables.description` | body | `string` | no | Optional project description. |
