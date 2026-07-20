# Cancel Bulk Email Verification Batch with Clearout

Cancels a running bulk email verification batch in Clearout.

## Endpoint

- **Method:** `POST`
- **Path:** `/email_verify/list/cancel`
- **Base URL:** `https://api.clearout.io/v2`
- **Official documentation:** [Cancel Bulk Email Verification Batch](https://docs.clearout.io/developers/api/email-verify)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | body | `string` | yes | Pass the value of bulk list_id property from response object |
