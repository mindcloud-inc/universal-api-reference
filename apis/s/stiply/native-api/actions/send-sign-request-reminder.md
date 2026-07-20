# Send Sign Request Reminder with Stiply

Sends a reminder for a Stiply sign request.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/sign_requests/:sign_request/actions/send_reminder`
- **Base URL:** `https://api.stiply.nl`
- **Official documentation:** [Send Sign Request Reminder](https://app.stiply.nl/api-documentation/v2#tag/sign-requests/operation/SendSignRequestReminder)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sign_request` | path | `number` | yes | Id of the signrequest. |
