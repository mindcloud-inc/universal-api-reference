# List Responses with Typeform

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:formId/responses`
- **Base URL:** `https://api.typeform.com`
- **Official documentation:** [List Responses](https://www.typeform.com/developers/responses/reference/retrieve-responses/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `excluded_response_ids` | query | `string` | no | — |
| `formId` | path | `list` | yes | Typeform form ID. |
| `response_type` | query | `string` | no | — |
| `sort` | query | `string` | no | — |
| `since` | query | `date` | no | Return responses submitted after this date/time. |
| `until` | query | `date` | no | Return responses submitted before this date/time. |
| `after` | query | `string` | no | Cursor token for next page of responses. |
| `before` | query | `string` | no | Cursor token for previous page of responses. |
| `completed` | query | `boolean` | no | Filter by completion status. |
| `query` | query | `string` | no | Search responses by text. |
| `fields` | query | `string` | no | Filter on specific field IDs. Send multiple values as a string separated by `,`. |
| `answered_fields` | query | `string` | no | Filter by answered field IDs. Send multiple values as a string separated by `,`. |
| `included_response_ids` | query | `string` | no | Only include specific response IDs. Send multiple values as a string separated by `,`. |
