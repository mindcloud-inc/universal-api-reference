# Send Session SMS Invitation with LogMeIn

Sends a session SMS invitation from LogMeIn.

## Endpoint

- **Method:** `POST`
- **Path:** `/goto-resolve/v1/sessions/:sessionId/invite/sms`
- **Base URL:** `https://api.goto.com`
- **Official documentation:** [Send Session SMS Invitation](https://developer.goto.com/LogMeInResolve/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sessionId` | path | `string` | yes | Required session ID for the SMS invitation. |
| `language` | body | `string` | yes | Invitation language code such as EN, DE, ES, FR, HU, IT, PT, NL, JA, TW, CN, KR, or TH. |
| `phoneNumber` | body | `string` | yes | Phone number to send the session invitation to. |
