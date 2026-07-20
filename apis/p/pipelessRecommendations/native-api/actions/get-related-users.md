# Get Related Users with Pipeless Recommendations

Retrieves related users in Pipeless Recommendations.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/apps/:appId/algos/recommendations/related-users`
- **Base URL:** `https://api.pipeless.io`
- **Official documentation:** [Get Related Users](https://docs.pipeless.io/reference/get-related-users)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Numeric Pipeless app ID. |
| `object.id` | body | `string` | yes | — |
| `object.type` | body | `string` | yes | — |
| `followed_relationship_type` | body | `string` | yes | — |
| `content_tagged_relationship_type` | body | `string` | yes | — |
