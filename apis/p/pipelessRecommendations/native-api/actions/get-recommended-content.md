# Get Recommended Content with Pipeless Recommendations

Retrieves recommended content in Pipeless Recommendations.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/apps/:appId/algos/recommendations/content`
- **Base URL:** `https://api.pipeless.io`
- **Official documentation:** [Get Recommended Content](https://docs.pipeless.io/reference/get-recommended-content)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Numeric Pipeless app ID. |
| `object.id` | body | `string` | yes | Target object ID. |
| `object.type` | body | `string` | yes | Target object type. |
| `content_object_type` | body | `string` | yes | Object type to recommend. |
| `primary_positive_relationship_type` | body | `string` | yes | Primary positive relationship type. |
| `primary_negative_relationship_type` | body | `string` | yes | Primary negative relationship type. |
| `content_tagged_relationship_type` | body | `string` | yes | Relationship type connecting content to tags. |
| `content_tag_object_type` | body | `string` | yes | Object type used for tags. |
| `limit` | body | `string` | no | Maximum number of results. |
