# Update Twilio provider with Appwrite

Updates the twilio provider in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/messaging/providers/twilio/{providerId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update Twilio provider](https://appwrite.io/docs/references/cloud/server-rest/messaging)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `providerId` | path | `string` | yes | Provider ID. |
| `name` | body | `string` | no | Provider name. |
| `enabled` | body | `boolean` | no | Set as enabled. |
| `accountSid` | body | `string` | no | Twilio account secret ID. |
| `authToken` | body | `string` | no | Twilio authentication token. |
| `from` | body | `string` | no | Sender number. |
