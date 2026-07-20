# Update Target App with Statsig

Updates a target app in Statsig.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/console/v1/target_app/{id}`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Update Target App](https://docs.statsig.com/api-reference/target-app/update-target-app)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | id |
| `name` | body | `string` | no | Request body field. |
| `description` | body | `string` | no | Request body field. |
