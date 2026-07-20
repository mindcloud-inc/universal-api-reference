# Update Waiver Note with WaiverForever

Updates a waiver note in WaiverForever.

## Endpoint

- **Method:** `POST`
- **Path:** `/openapi/v1/waiver/:waiver_id/note`
- **Base URL:** `https://api.waiverforever.com`
- **Official documentation:** [Update Waiver Note](https://docs.waiverforever.com/#update-waiver-note)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `note` | body | `string` | yes | Updated waiver note text. |
| `waiver_id` | path | `string` | yes | Signed waiver identifier. |
