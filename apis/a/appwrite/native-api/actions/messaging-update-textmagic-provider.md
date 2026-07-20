# Update Textmagic provider with Appwrite

Updates the textmagic provider in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/messaging/providers/textmagic/{providerId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update Textmagic provider](https://appwrite.io/docs/references/cloud/server-rest/messaging)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `providerId` | path | `string` | yes | Provider ID. |
| `name` | body | `string` | no | Provider name. |
| `enabled` | body | `boolean` | no | Set as enabled. |
| `username` | body | `string` | no | Textmagic username. |
| `apiKey` | body | `string` | no | Textmagic apiKey. |
| `from` | body | `string` | no | Sender number. |
