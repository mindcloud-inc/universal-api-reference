# Get Waiver Request with WaiverForever

Retrieves a waiver request from WaiverForever.

## Endpoint

- **Method:** `GET`
- **Path:** `/openapi/v2/waiverRequest/:waiver_request_id`
- **Base URL:** `https://api.waiverforever.com`
- **Official documentation:** [Get Waiver Request](https://docs.waiverforever.com/#get-waiver-request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_waivers` | query | `boolean` | no | Include submitted waivers in the response. |
| `waiver_request_id` | path | `string` | yes | Waiver request group identifier. |
