# Get Sorted Content with Pipeless Recommendations

Ranks supplied content in Pipeless Recommendations for a target object.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/apps/:appId/algos/recommendations/sorted-content`
- **Base URL:** `https://api.pipeless.io`
- **Official documentation:** [Get Sorted Content](https://docs.pipeless.io/reference/getsortedcontent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `string` | yes | Numeric Pipeless app ID. |
| `object.id` | body | `string` | yes | — |
| `object.type` | body | `string` | yes | — |
| `primary_positive_relationship_type` | body | `string` | yes | — |
| `content_tagged_relationship_type` | body | `string` | yes | — |
| `content_tag_object_type` | body | `string` | yes | — |
| `content_object_type` | body | `string` | yes | — |
| `content_ids[0]` | body | `string` | yes | — |
| `content_ids[1]` | body | `string` | yes | — |
