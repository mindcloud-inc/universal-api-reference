# Create Target App with Statsig

Creates a target app in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/console/v1/target_app`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Create Target App](https://docs.statsig.com/api-reference/target-app/create-target-app)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Request body field. |
| `description` | body | `string` | yes | Request body field. |
| `gates` | body | `list` | no | Request body field. |
| `dynamicConfigs` | body | `list` | no | Request body field. |
| `experiments` | body | `list` | no | Request body field. |
