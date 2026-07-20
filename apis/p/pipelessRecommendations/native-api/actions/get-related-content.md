# Get Related Content with Pipeless Recommendations

Retrieves related content in Pipeless Recommendations.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/apps/:appId/algos/recommendations/related-content`
- **Base URL:** `https://api.pipeless.io`
- **Official documentation:** [Get Related Content](https://docs.pipeless.io/reference/get-related-content)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Numeric Pipeless app ID. |
| `object.id` | body | `string` | yes | — |
| `object.type` | body | `string` | yes | — |
| `positive_rel` | body | `string` | yes | — |
| `content_tagged_object_type` | body | `string` | yes | — |
| `content_tagged_relationship_type` | body | `string` | yes | — |
