# Copy App with Qlik

Creates a copy of an app in Qlik.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/apps/:appId/copy`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [Copy App](https://qlik.dev/apis/rest/apps/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Qlik app ID. |
| `name` | body | `string` | no | Name for the copied Qlik app. |
