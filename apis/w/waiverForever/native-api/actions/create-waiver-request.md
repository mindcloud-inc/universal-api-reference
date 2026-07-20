# Create Waiver Request with WaiverForever

Creates a waiver request in WaiverForever.

## Endpoint

- **Method:** `POST`
- **Path:** `/openapi/v2/waiverRequest`
- **Base URL:** `https://api.waiverforever.com`
- **Official documentation:** [Create Waiver Request](https://docs.waiverforever.com/#create-waiver-request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_info` | body | `string` | no | Optional contact information for the request group. |
| `name` | body | `string` | yes | Waiver request group name. |
| `note` | body | `string` | no | Optional request note. |
| `size` | body | `number` | yes | Number of recipients to create in the request group. |
| `template_id` | body | `string` | yes | Template used by the waiver request. |
| `type` | body | `string` | no | Request type such as normal or anonymous. |
