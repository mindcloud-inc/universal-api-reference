# Update Vonage provider with Appwrite

Updates the vonage provider in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/messaging/providers/vonage/{providerId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update Vonage provider](https://appwrite.io/docs/references/cloud/server-rest/messaging)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `providerId` | path | `string` | yes | Provider ID. |
| `name` | body | `string` | no | Provider name. |
| `enabled` | body | `boolean` | no | Set as enabled. |
| `apiKey` | body | `string` | no | Vonage API key. |
| `apiSecret` | body | `string` | no | Vonage API secret. |
| `from` | body | `string` | no | Sender number. |
