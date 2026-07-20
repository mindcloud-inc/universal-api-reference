# Start Personal Plan Request with White Swan

Starts a personal plan request in White Swan.

## Endpoint

- **Method:** `POST`
- **Path:** `/new_request`
- **Base URL:** `https://app.whiteswan.io/api/1.1/wf`
- **Official documentation:** [Start Personal Plan Request](https://docs.whiteswan.io/partner-knowledge-base/api-documentation/action-calls/start-personal-plan-request)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Applicant full name. |
| `email` | body | `string` | no | Applicant email address. |
| `phone` | body | `string` | no | Applicant phone number. |
| `policy_type` | body | `string` | no | Requested policy type. |
| `main_goal` | body | `string` | no | Primary plan goal. |
| `resident_state` | body | `string` | no | Applicant resident state. |
| `death_benefit` | body | `number` | no | Requested death benefit. |
| `payment_schedule` | body | `string` | no | Preferred payment schedule. |
| `paid_up_period` | body | `string` | no | Paid-up period for permanent policy requests. |
| `term_duration` | body | `string` | no | Requested term duration. |
| `premium_budget` | body | `number` | no | Monthly or scheduled premium budget. |
| `gender` | body | `string` | no | Applicant gender. |
| `health_rating` | body | `string` | no | Underwriting health rating. |
| `date_of_birth` | body | `string` | no | Applicant date of birth in White Swan format. |
| `tobacco` | body | `boolean` | no | Whether the applicant uses tobacco. |
| `marijuana` | body | `boolean` | no | Whether the applicant uses marijuana. |
| `height_feet` | body | `number` | no | Applicant height in feet. |
| `height_inches` | body | `number` | no | Applicant remaining height in inches. |
| `weight_pounds` | body | `number` | no | Applicant weight in pounds. |
| `convertability` | body | `boolean` | no | Whether the term should be convertible. |
| `associated_person` | body | `string` | no | White Swan user email to associate with the request. |
| `request_comment` | body | `string` | no | Internal comment to attach to the request. |
