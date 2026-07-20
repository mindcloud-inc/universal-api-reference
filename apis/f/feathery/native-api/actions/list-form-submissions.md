# List Form Submissions with Feathery

## Endpoint

- **Method:** `GET`
- **Path:** `/api/form/submission/`
- **Base URL:** `https://api.feathery.io`
- **Official documentation:** [List Form Submissions](https://api-docs.feathery.io/#list-form-submissions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_id` | query | `string` | yes | The ID of the form to get submission data for. |
| `start_time` | query | `date` | no | Limit submissions to after this update time. |
| `end_time` | query | `date` | no | Limit submissions to before this update time. |
| `created_after` | query | `date` | no | Limit submissions to after this creation time. |
| `created_before` | query | `date` | no | Limit submissions to before this creation time. |
| `count` | query | `number` | no | Limit the number of returned submissions. |
| `completed` | query | `boolean` | no | Only fetch submissions that are either completed or incomplete. |
| `field_search` | query | `string` | no | Stringified JSON array of field-value match objects. |
| `fuzzy_search` | query | `string` | no | Stringified JSON object describing fuzzy search options. |
| `fields` | query | `string` | no | Comma-separated list of field IDs to include in the response. |
| `no_field_values` | query | `boolean` | no | If true, do not return field data. |
| `sort` | query | `string` | no | Sort returned field values, for example by layout. |
| `page_size` | query | `number` | no | Maximum number of submissions to return in one page. |
| `use_cache` | query | `boolean` | no | If true, fetch results from the cached source for lower latency. |
