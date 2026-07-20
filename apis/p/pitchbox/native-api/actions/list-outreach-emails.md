# List Outreach Emails with Pitchbox

## Endpoint

- **Method:** `GET`
- **Path:** `/api/outreach_emails`
- **Base URL:** `https://apiv2.pitchbox.com`
- **Official documentation:** [List Outreach Emails](https://apiv2.pitchbox.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sent_at_from` | query | `string` | yes | Filter outreach emails from this date/time. |
| `sent_at_to` | query | `string` | yes | Filter outreach emails up to this date/time. |
