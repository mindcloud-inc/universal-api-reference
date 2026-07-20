# Get Activity On Object with Pipeless Recommendations

Retrieves activity on a target object in Pipeless Recommendations.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/apps/:appId/algos/activity/object`
- **Base URL:** `https://api.pipeless.io`
- **Official documentation:** [Get Activity On Object](https://docs.pipeless.io/reference/get-activity-on-object)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Numeric Pipeless app ID. |
| `object.id` | body | `string` | yes | Target object ID. |
| `object.type` | body | `string` | yes | Target object type. |
