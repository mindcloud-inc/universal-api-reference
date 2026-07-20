# List Routing Form Submissions with Calendly

Retrieves routing form submissions from Calendly.

## Endpoint

- **Method:** `GET`
- **Path:** `/routing_form_submissions`
- **Base URL:** `https://api.calendly.com`
- **Official documentation:** [List Routing Form Submissions](https://developer.calendly.com/api-docs)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form` | query | `string` | yes | Routing form URI filter. |
| `sort` | query | `list` | no | Sort order for routing form submissions. Accepted values: `created_at:asc`, `created_at:desc`. |
