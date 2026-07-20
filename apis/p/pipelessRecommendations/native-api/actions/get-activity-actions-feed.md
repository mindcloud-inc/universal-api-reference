# Get Activity Actions Feed with Pipeless Recommendations

Retrieves grouped activity actions for an object in Pipeless Recommendations.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/apps/:appId/algos/activity/actions-feed`
- **Base URL:** `https://api.pipeless.io`
- **Official documentation:** [Get Activity Actions Feed](https://docs.pipeless.io/reference/get-activity-actions-feed)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Numeric Pipeless app ID. |
| `object.id` | body | `string` | yes | — |
| `object.type` | body | `string` | yes | — |
