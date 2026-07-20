# Send onboarding test mail using dedicated test domains with Maildrip

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/onboarding/test-email`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Send onboarding test mail using dedicated test domains](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subject` | body | `string` | yes | — |
| `body` | body | `string` | yes | — |
| `recipients[]` | body | `array<string>` | no | Send multiple values as a array. |
| `fromName` | body | `string` | no | — |
| `replyTo` | body | `string` | no | — |
| `attachments[]` | body | `array<object>` | no | Send multiple values as a array. |
