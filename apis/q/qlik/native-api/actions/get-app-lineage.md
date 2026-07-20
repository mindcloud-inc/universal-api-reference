# Get App Lineage with Qlik

Retrieves lineage data for an app in Qlik.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/apps/:appId/data/lineage`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [Get App Lineage](https://qlik.dev/apis/rest/apps/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Qlik app ID. |
