# Create Msg91 provider with Appwrite

Creates a new Msg91 provider in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/messaging/providers/msg91`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create Msg91 provider](https://appwrite.io/docs/references/cloud/server-rest/messaging)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `providerId` | body | `string` | yes | Provider ID. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `name` | body | `string` | yes | Provider name. |
| `templateId` | body | `string` | no | Msg91 template ID |
| `senderId` | body | `string` | no | Msg91 sender ID. |
| `authKey` | body | `string` | no | Msg91 auth key. |
| `enabled` | body | `boolean` | no | Set as enabled. |
