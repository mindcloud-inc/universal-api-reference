# Get Attributes with ThingsBoard

Retrieves attributes for a specific entity from ThingsBoard.

## Endpoint

- **Method:** `GET`
- **Path:** `/plugins/telemetry/:entityType/:entityId/values/attributes`
- **Base URL:** `{baseUrl}/api`
- **Official documentation:** [Get Attributes](https://thingsboard.cloud/swagger-ui/index.html#/telemetry-controller/getAttributes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entityType` | path | `string` | yes | The ThingsBoard entity type, for example DEVICE. |
| `entityId` | path | `string` | yes | The ThingsBoard entity ID. |
| `params` | query | `string` | yes | Additional provider-specific telemetry query parameters. |
