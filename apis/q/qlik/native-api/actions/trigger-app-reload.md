# Trigger App Reload with Qlik

Triggers an app reload in Qlik.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/reloads`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [Trigger App Reload](https://qlik.dev/apis/rest/reloads/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | body | `string` | yes | Qlik app ID to reload. |
| `partial` | body | `boolean` | no | Whether to perform a partial reload. |
| `variables` | body | `object` | no | Reload variables object. |
