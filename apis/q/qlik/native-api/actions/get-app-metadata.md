# Get App Metadata with Qlik

Retrieves metadata for an app in Qlik.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/apps/:appId/data/metadata`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [Get App Metadata](https://qlik.dev/apis/rest/apps/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Qlik app ID. |
