# Download Bulk Email Finder Result with Clearout

Retrieves a bulk email finder result download from Clearout.

## Endpoint

- **Method:** `POST`
- **Path:** `/email_finder/download/result`
- **Base URL:** `https://api.clearout.io/v2`
- **Official documentation:** [Download Bulk Email Finder Result](https://docs.clearout.io/developers/api/email-finder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | body | `string` | yes | Pass the value of bulk list_id property from response object |
