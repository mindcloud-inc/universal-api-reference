# List Responses with SurveySparrow

Retrieves all responses from SurveySparrow.

## Endpoint

- **Method:** `GET`
- **Path:** `/responses`
- **Base URL:** `https://api.surveysparrow.com/v3`
- **Official documentation:** [List Responses](https://developers.surveysparrow.com/rest-apis/get-v-3-responses/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `survey_id` | query | `number` | yes | ID of the survey. |
| `contact_id` | query | `number` | no | Filter responses by contact ID. |
| `state` | query | `list` | no | Filter responses by submission state. Accepted values: `0`, `1`, `2`. |
| `order_by` | query | `list` | no | Field to sort responses by. Accepted values: `0`, `1`, `2`. |
| `order` | query | `list` | no | Sort direction. Accepted values: `0`, `1`. |
| `preserve_format` | query | `boolean` | no | Preserve formatted response values. |
| `response_url` | query | `boolean` | no | Include response URLs. |
| `date.gte` | query | `date` | no | Filter responses by completion date on or after this date. |
| `date.lte` | query | `date` | no | Filter responses by completion date on or before this date. |
| `created_date.gte` | query | `date` | no | Filter responses created on or after this date. |
| `created_date.lte` | query | `date` | no | Filter responses created on or before this date. |
