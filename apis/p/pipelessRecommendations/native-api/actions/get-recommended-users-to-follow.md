# Get Recommended Users To Follow with Pipeless Recommendations

Retrieves recommended users to follow in Pipeless Recommendations.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/apps/:appId/algos/recommendations/users-to-follow`
- **Base URL:** `https://api.pipeless.io`
- **Official documentation:** [Get Recommended Users To Follow](https://docs.pipeless.io/reference/get-recommended-users-to-follow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Numeric Pipeless app ID. |
| `object.id` | body | `string` | yes | — |
| `object.type` | body | `string` | yes | — |
| `followed_relationship_type` | body | `string` | yes | — |
| `positive_relationship_type` | body | `string` | yes | — |
| `content_tagged_relationship_type` | body | `string` | yes | — |
| `content_object_type` | body | `string` | yes | — |
| `content_tag_object_type` | body | `string` | yes | — |
