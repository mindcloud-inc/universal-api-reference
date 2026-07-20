# List Signature Requests with Yousign

Retrieves signature requests from Yousign.

## Endpoint

- **Method:** `GET`
- **Path:** `/signature_requests`
- **Base URL:** `https://api-sandbox.yousign.app/v3`
- **Official documentation:** [List Signature Requests](https://developers.yousign.com/reference/get-signature_requests-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `after` | query | `string` | no | Pagination cursor. |
| `limit` | query | `number` | no | Maximum signature requests to return. |
| `q` | query | `string` | no | Search on signature request name. |
| `status[eq]` | query | `string` | no | Return only signature requests with this exact status. |
| `created_at[after]` | query | `string` | no | Return only signature requests created after this date (yyyy-mm-dd). |
| `created_at[before]` | query | `string` | no | Return only signature requests created before this date (yyyy-mm-dd). |
| `workspace_id[eq]` | query | `string` | no | Return only signature requests in this workspace. |
| `external_id[eq]` | query | `string` | no | Return only signature requests with this external ID. |
| `source[eq]` | query | `string` | no | Return only signature requests created from this source. |
| `label.name[eq]` | query | `string` | no | Return only signature requests with a label that exactly matches this name. |
