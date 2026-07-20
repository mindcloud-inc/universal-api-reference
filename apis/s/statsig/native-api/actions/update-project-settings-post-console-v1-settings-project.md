# Update Project Settings with Statsig

Updates project settings in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/settings/project`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Update Project Settings](https://docs.statsig.com/api-reference/settings/update-project-settings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Request body field. |
| `visibility` | body | `string` | yes | Request body field. |
| `default_unit_type` | body | `string` | no | Request body field. |
