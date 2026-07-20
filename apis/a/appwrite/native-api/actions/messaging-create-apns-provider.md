# Create APNS provider with Appwrite

Creates a new APNS provider in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/messaging/providers/apns`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create APNS provider](https://appwrite.io/docs/references/cloud/server-rest/messaging)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `providerId` | body | `string` | yes | Provider ID. Choose a custom ID or generate a random ID with `ID.unique()`. Valid chars are a-z, A-Z, 0-9, period, hyphen, and underscore. Can't start with a special char. Max length is 36 chars. |
| `name` | body | `string` | yes | Provider name. |
| `authKey` | body | `string` | no | APNS authentication key. |
| `authKeyId` | body | `string` | no | APNS authentication key ID. |
| `teamId` | body | `string` | no | APNS team ID. |
| `bundleId` | body | `string` | no | APNS bundle ID. |
| `sandbox` | body | `boolean` | no | Use APNS sandbox environment. |
| `enabled` | body | `boolean` | no | Set as enabled. |
