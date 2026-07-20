# List Waiver Requests with WaiverForever

Retrieves waiver requests from WaiverForever.

## Endpoint

- **Method:** `GET`
- **Path:** `/openapi/v2/waiverRequests`
- **Base URL:** `https://api.waiverforever.com`
- **Official documentation:** [List Waiver Requests](https://docs.waiverforever.com/#list-waiver-requests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end_timestamp` | query | `number` | no | End timestamp in seconds. |
| `include_waivers` | query | `boolean` | no | Include submitted waivers in the response. |
| `name` | query | `string` | no | Optional name filter. |
| `page` | query | `number` | no | Results page number. |
| `per_page` | query | `number` | no | Results returned per page. |
| `request_ids` | query | `list<string>` | no | Specific waiver request ids to include. Send multiple values as a array. |
| `start_timestamp` | query | `number` | no | Start timestamp in seconds. |
| `status` | query | `string` | no | Optional status filter such as collecting or accepted. |
| `template_id` | query | `string` | yes | Template whose waiver requests should be listed. |
