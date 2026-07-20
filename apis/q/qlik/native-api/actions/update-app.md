# Update App with Qlik

Updates an existing app in Qlik.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/apps/:appId`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [Update App](https://qlik.dev/apis/rest/apps/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Qlik app ID. |
| `name` | body | `string` | no | Updated Qlik app name. |
