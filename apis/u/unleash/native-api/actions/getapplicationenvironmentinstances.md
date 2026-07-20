# Get Application Environment Instances (Last 24H) with Unleash

Retrieves application environment instances (Last 24h) from Unleash.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/admin/metrics/instances/{appName}/environment/{environment}`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [Get Application Environment Instances (Last 24H)](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appName` | path | `string` | yes | Required path parameter. |
| `environment` | path | `string` | yes | Required path parameter. |
