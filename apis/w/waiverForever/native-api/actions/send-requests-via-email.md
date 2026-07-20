# Send Requests via Email with WaiverForever

Sends waiver requests by email from WaiverForever.

## Endpoint

- **Method:** `POST`
- **Path:** `/openapi/v2/waiverRequests/sendGroupEmail`
- **Base URL:** `https://api.waiverforever.com`
- **Official documentation:** [Send Requests via Email](https://docs.waiverforever.com/#send-requests-via-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email_note` | body | `string` | no | Optional note included in the outbound email. |
| `expired_in` | body | `number` | no | Expiration timestamp for the email request. |
| `group_id` | body | `string` | yes | Waiver request group to email. |
| `prefill_list` | body | `list<object>` | no | Recipient objects with `name`, `email`, and optional prefill field values from the request prefill schema. Send multiple values as a array. |
| `recipient_list` | body | `string` | no | Recipient list string for delivery, for example `email<display>`. Use either this field or `Prefill List`. |
| `reply_to` | body | `string` | yes | Reply-to email address. Runtime verification showed this account requires a provider-accepted mailbox. |
