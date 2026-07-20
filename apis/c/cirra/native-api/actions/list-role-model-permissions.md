# List Role Model Permissions with Cirra

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/cirra/roles/:roleId/permissions/apps/:appId/models`
- **Base URL:** `http://api-public:9801`

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `roleId` | path | `list` | yes |
| `appId` | path | `string` | yes |
