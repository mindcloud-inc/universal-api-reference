# Download Bulk Email Verification Result with Clearout

Retrieves a bulk email verification result download from Clearout.

## Endpoint

- **Method:** `POST`
- **Path:** `/download/result`
- **Base URL:** `https://api.clearout.io/v2`
- **Official documentation:** [Download Bulk Email Verification Result](https://docs.clearout.io/developers/api/email-verify)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | body | `string` | yes | Pass the value of bulk list_id property from response object |
