# Cancel Bulk Email Finder Batch with Clearout

Cancels a running bulk email finder batch in Clearout.

## Endpoint

- **Method:** `POST`
- **Path:** `/email_finder/list/cancel`
- **Base URL:** `https://api.clearout.io/v2`
- **Official documentation:** [Cancel Bulk Email Finder Batch](https://docs.clearout.io/developers/api/email-finder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | body | `string` | yes | Pass the value of bulk list_id property from response object |
