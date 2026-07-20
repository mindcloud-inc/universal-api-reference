# Edit Waiver Request with WaiverForever

Updates a waiver request in WaiverForever.

## Endpoint

- **Method:** `POST`
- **Path:** `/openapi/v2/waiverRequest/:waiver_request_id`
- **Base URL:** `https://api.waiverforever.com`
- **Official documentation:** [Edit Waiver Request](https://docs.waiverforever.com/#edit-waiver-request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_info` | body | `string` | no | Updated contact information. |
| `name` | body | `string` | yes | Updated waiver request group name. |
| `note` | body | `string` | no | Updated request note. |
| `size` | body | `number` | yes | Updated request group size. |
| `waiver_request_id` | path | `string` | yes | Waiver request group identifier. |
