# Get Recent Events with Pipeless Recommendations

Retrieves recent events from Pipeless Recommendations.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/apps/:appId/recent-events`
- **Base URL:** `https://api.pipeless.io`
- **Official documentation:** [Get Recent Events](https://docs.pipeless.io/reference/get-recent-events)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Numeric Pipeless app ID for the target recommendation app. |
