# Get Activity Feed with Pipeless Recommendations

Retrieves an activity feed for an object in Pipeless Recommendations.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/apps/:appId/algos/activity/feed`
- **Base URL:** `https://api.pipeless.io`
- **Official documentation:** [Get Activity Feed](https://docs.pipeless.io/reference/get-activity-feed)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Numeric Pipeless app ID. |
| `object.id` | body | `string` | yes | — |
| `object.type` | body | `string` | yes | — |
