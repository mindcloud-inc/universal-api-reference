# List Reloads with Qlik

Retrieves reloads from your Qlik tenant.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/reloads`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [List Reloads](https://qlik.dev/apis/rest/reloads/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | query | `string` | yes | Qlik app ID to list reloads for. |
