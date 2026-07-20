# Update APNS provider with Appwrite

Updates the APNS provider in your Appwrite project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/messaging/providers/apns/{providerId}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Update APNS provider](https://appwrite.io/docs/references/cloud/server-rest/messaging)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `providerId` | path | `string` | yes | Provider ID. |
| `name` | body | `string` | no | Provider name. |
| `enabled` | body | `boolean` | no | Set as enabled. |
| `authKey` | body | `string` | no | APNS authentication key. |
| `authKeyId` | body | `string` | no | APNS authentication key ID. |
| `teamId` | body | `string` | no | APNS team ID. |
| `bundleId` | body | `string` | no | APNS bundle ID. |
| `sandbox` | body | `boolean` | no | Use APNS sandbox environment. |
