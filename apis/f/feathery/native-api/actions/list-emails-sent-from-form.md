# List Emails Sent From Form with Feathery

## Endpoint

- **Method:** `GET`
- **Path:** `/api/logs/email/form/:form_id/`
- **Base URL:** `https://api.feathery.io`
- **Official documentation:** [List Emails Sent From Form](https://api-docs.feathery.io/#list-emails-sent-from-form)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_id` | path | `string` | yes | The ID of the form whose outbound emails you want to inspect. |
| `start_time` | query | `date` | no | Only return emails sent after this time. |
| `end_time` | query | `date` | no | Only return emails sent before this time. |
