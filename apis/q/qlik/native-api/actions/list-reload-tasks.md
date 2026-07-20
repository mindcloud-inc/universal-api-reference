# List Reload Tasks with Qlik

Retrieves reload tasks from your Qlik tenant.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/reload-tasks`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [List Reload Tasks](https://qlik.dev/apis/rest/reload-tasks/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | query | `string` | no | Optional Qlik app ID to filter reload tasks. |
