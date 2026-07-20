# List Personal Plans with White Swan

Retrieves personal plans from White Swan.

## Endpoint

- **Method:** `POST`
- **Path:** `/personal_plan`
- **Base URL:** `https://app.whiteswan.io/api/1.1/wf`
- **Official documentation:** [List Personal Plans](https://docs.whiteswan.io/partner-knowledge-base/api-documentation/information-calls/personal-plan-s)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `plan_id` | body | `string` | no | Filter personal plans by White Swan plan ID. |
| `policy_search` | body | `string` | no | Filter personal plans by policy search ID. |
| `user_email` | body | `string` | no | Filter personal plans by account user email. |
| `client_email` | body | `string` | no | Filter personal plans by client email. |
