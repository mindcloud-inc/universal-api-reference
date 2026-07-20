# List Responses with Fairing

Retrieves responses from Fairing.

## Endpoint

- **Method:** `GET`
- **Path:** `/responses`
- **Base URL:** `https://app.fairing.co/api`
- **Official documentation:** [List Responses](https://docs.fairing.co/reference/retrieve-responses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `question_id` | query | `number` | no | Only return responses for the specified Fairing question ID. |
| `since` | query | `date` | no | ISO8601 timestamp used to fetch responses newer than this value. |
| `until` | query | `date` | no | ISO8601 timestamp used to fetch responses older than this value. |
| `before` | query | `string` | no | Response ID cursor used to fetch the page before the referenced response. |
| `after` | query | `string` | no | Response ID cursor used to fetch the page after the referenced response. |
