# Update Msg91 provider with Appwrite

Updates the Msg91 provider in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/messaging/providers/msg91/{providerId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update Msg91 provider](https://appwrite.io/docs/references/cloud/server-rest/messaging)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `providerId` | path | `string` | yes | Provider ID. |
| `name` | body | `string` | no | Provider name. |
| `enabled` | body | `boolean` | no | Set as enabled. |
| `templateId` | body | `string` | no | Msg91 template ID. |
| `senderId` | body | `string` | no | Msg91 sender ID. |
| `authKey` | body | `string` | no | Msg91 auth key. |
