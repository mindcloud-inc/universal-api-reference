# Create Call with Avoma

Creates a new call in Avoma.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/calls/`
- **Base URL:** `https://api.avoma.com`
- **Official documentation:** [Create Call](https://dev.avoma.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `external_id` | body | `string` | yes | Unique ID of the call from the dialer system. |
| `user_email` | body | `string` | yes | Email of the Avoma user who made or received the call. |
| `frm` | body | `string` | yes | Phone number from which the call was made. |
| `to` | body | `string` | yes | Phone number to which the call was made. |
| `start_at` | body | `string` | yes | Start time of the call in ISO 8601 UTC format. |
| `recording_url` | body | `string` | yes | Public URL of the call recording for Avoma to download and process. |
| `direction` | body | `string` | yes | Direction of the call, for example inbound or outbound. |
| `source` | body | `string` | yes | Lowercase source of the call, for example ringcentral or twilio. |
| `participants[].email` | body | `string` | yes | Email address of a participant. The first participant should be the prospect or lead. |
| `participants[].name` | body | `string` | no | Name of a participant. |
| `subject` | body | `string` | no | Subject of the meeting associated with the call. |
| `meeting_purpose_uuid` | body | `string` | no | UUID of the meeting type associated with the call. |
| `meeting_outcome_uuid` | body | `string` | no | UUID of the meeting outcome associated with the call. |
