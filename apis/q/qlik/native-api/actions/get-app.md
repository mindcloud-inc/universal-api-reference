# Get App with Qlik

Retrieves an app from your Qlik tenant.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/apps/:appId`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [Get App](https://qlik.dev/apis/rest/apps/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Qlik app ID. |
