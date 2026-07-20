# List Form Responses with Moaform

Retrieves responses for a form in Moaform.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:formId/responses`
- **Base URL:** `https://api.moaform.com/v1`
- **Official documentation:** [List Form Responses](https://help.moaform.com/hc/en-us/articles/28407667571097-Fetching-Form-Responses)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_id` | path | `string` | yes | Unique ID of the form. |
| `since` | query | `string` | no | Only return responses submitted after this timestamp. |
| `until` | query | `string` | no | Only return responses submitted before this timestamp. |
| `after` | query | `string` | no | Only return responses submitted after this response ID. |
| `before` | query | `string` | no | Only return responses submitted before this response ID. |
| `included_response_ids` | query | `string` | no | Comma-separated response IDs to include. |
| `excluded_response_ids` | query | `string` | no | Comma-separated response IDs to exclude. |
