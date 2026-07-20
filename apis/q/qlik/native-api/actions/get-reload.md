# Get Reload with Qlik

Retrieves a reload from your Qlik tenant.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/reloads/:reloadId`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [Get Reload](https://qlik.dev/apis/rest/reloads/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reloadId` | path | `string` | yes | Qlik reload ID. |
