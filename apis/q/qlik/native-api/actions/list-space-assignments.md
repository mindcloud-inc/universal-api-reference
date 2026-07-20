# List Space Assignments with Qlik

Retrieves assignments for a space in Qlik.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/spaces/:spaceId/assignments`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [List Space Assignments](https://qlik.dev/apis/rest/spaces/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `spaceId` | path | `string` | yes | Qlik space ID. |
