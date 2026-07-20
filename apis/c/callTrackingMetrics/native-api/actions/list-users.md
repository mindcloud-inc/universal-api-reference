# List Users with CallTrackingMetrics

Retrieves users for an account from CallTrackingMetrics.

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts/:accountId/users.json`
- **Base URL:** `https://api.calltrackingmetrics.com/api/v1`
- **Official documentation:** [List Users](https://www.postman.com/ctm-8695/calltrackingmetrics-s-public-workspace/request/emrginr/list-of-users)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Filter users by email address. |
| `filter` | query | `string` | no | Filter users by status or scope. |
