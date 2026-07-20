# Get Health Status with EyeLevel.ai

Retrieves a service health status from EyeLevel.ai.

## Endpoint

- **Method:** `GET`
- **Path:** `/health/:service`
- **Base URL:** `https://api.groundx.ai/api/v1`
- **Official documentation:** [Get Health Status](https://docs.eyelevel.ai/reference/api-reference/health/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `service` | path | `string` | yes | The service name to inspect, such as search. |
