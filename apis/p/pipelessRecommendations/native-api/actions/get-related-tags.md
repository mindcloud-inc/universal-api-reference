# Get Related Tags with Pipeless Recommendations

Retrieves related tags in Pipeless Recommendations.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/apps/:appId/algos/recommendations/related-tags`
- **Base URL:** `https://api.pipeless.io`
- **Official documentation:** [Get Related Tags](https://docs.pipeless.io/reference/get-related-tags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Numeric Pipeless app ID. |
| `object.id` | body | `string` | yes | — |
| `object.type` | body | `string` | yes | — |
| `content_object_type` | body | `string` | yes | — |
