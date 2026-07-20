# Check Phone Status with ContactOut

Retrieves phone availability for a LinkedIn profile in ContactOut.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/people/linkedin/phone_status`
- **Base URL:** `https://api.contactout.com`
- **Official documentation:** [Check Phone Status](https://api.contactout.com/#phone-number-checker)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profile` | query | `string` | yes | The full LinkedIn profile URL. Must begin with http and contain linkedin.com/in/ or linkedin.com/pub/. |
