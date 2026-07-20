# Export App with Qlik

Exports an existing app from Qlik.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/apps/:appId/export`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [Export App](https://qlik.dev/apis/rest/apps/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Qlik app ID. |
| `NoData` | query | `boolean` | no | When true, export the app without data. |
