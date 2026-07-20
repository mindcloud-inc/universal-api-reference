# Bulk Assign Target Apps with Statsig

Bulk assigns target apps in Statsig.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/console/v1/target_app`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Bulk Assign Target Apps](https://docs.statsig.com/api-reference/target-app/bulk-assign-target-apps)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `targetApps` | body | `list` | yes | Request body field. |
| `gates` | body | `list` | no | Request body field. |
| `dynamicConfigs` | body | `list` | no | Request body field. |
| `experiments` | body | `list` | no | Request body field. |
