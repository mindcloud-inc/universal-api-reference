# Cancel Reload with Qlik

Cancels an existing reload in Qlik.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/reloads/:reloadId/actions/cancel`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [Cancel Reload](https://qlik.dev/apis/rest/reloads/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reloadId` | path | `string` | yes | Qlik reload ID. |
