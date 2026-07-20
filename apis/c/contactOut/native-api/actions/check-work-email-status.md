# Check Work Email Status with ContactOut

Retrieves work email availability for a LinkedIn profile in ContactOut.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/people/linkedin/work_email_status`
- **Base URL:** `https://api.contactout.com`
- **Official documentation:** [Check Work Email Status](https://api.contactout.com/#work-email-checker)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profile` | query | `string` | yes | The full LinkedIn profile URL. Must begin with http and contain linkedin.com/in/ or linkedin.com/pub/. |
