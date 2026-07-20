# Update Form Submission with CallRail

Updates a form submission in CallRail.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/a/:account_id/form_submissions/:form_submission_id.json`
- **Base URL:** `https://api.callrail.com`
- **Official documentation:** [Update Form Submission](https://apidocs.callrail.com/#updating-a-form-submission)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `account_id` | path | `string` | yes |
| `form_submission_id` | path | `string` | yes |
| `tags[]` | body | `array<string>` | no |
| `append_tags` | body | `boolean` | no |
| `lead_status` | body | `string` | no |
| `value` | body | `string` | no |
| `note` | body | `string` | no |
