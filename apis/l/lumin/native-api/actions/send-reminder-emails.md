# Send Reminder Emails with Lumin

## Endpoint

- **Method:** `POST`
- **Path:** `/signature_request/remind/:signature_request_id`
- **Base URL:** `https://api.luminpdf.com/v1`
- **Official documentation:** [Send Reminder Emails](https://developers.luminpdf.com/api/send-reminder-emails/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `signature_request_id` | path | `string` | yes | ID of the signature request. |
| `emails[]` | body | `array<string>` | yes | Array of signer email addresses to remind. |
