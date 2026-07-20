# List Plan Requests with White Swan

Retrieves plan requests from White Swan.

## Endpoint

- **Method:** `POST`
- **Path:** `/plan_requests`
- **Base URL:** `https://app.whiteswan.io/api/1.1/wf`
- **Official documentation:** [List Plan Requests](https://docs.whiteswan.io/partner-knowledge-base/api-documentation/information-calls/plan-request-s)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `request_id` | body | `string` | no | Filter plan requests by White Swan request ID. |
| `user_email` | body | `string` | no | Filter plan requests by account user email. |
| `client_email` | body | `string` | no | Filter plan requests by client email. |
