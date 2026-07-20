# List Sent Reply Emails with Pitchbox

## Endpoint

- **Method:** `GET`
- **Path:** `/api/sent_replies`
- **Base URL:** `https://apiv2.pitchbox.com`
- **Official documentation:** [List Sent Reply Emails](https://apiv2.pitchbox.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sent_at_from` | query | `string` | no | Filter sent replies from this date/time. |
| `sent_at_to` | query | `string` | no | Filter sent replies up to this date/time. |
