# Get Waiver Request Tracking Info with WaiverForever

Retrieves waiver request tracking info from WaiverForever.

## Endpoint

- **Method:** `GET`
- **Path:** `/openapi/v2/waiverRequests/groupTrackings`
- **Base URL:** `https://api.waiverforever.com`
- **Official documentation:** [Get Waiver Request Tracking Info](https://docs.waiverforever.com/#get-waiver-request-tracking-info)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_id` | query | `string` | yes | Waiver request group to inspect. |
| `page` | query | `number` | no | Results page number. |
| `per_page` | query | `number` | no | Results returned per page. |
