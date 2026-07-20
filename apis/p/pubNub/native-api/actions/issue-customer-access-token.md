# Issue Customer Access Token with PubNub

Issues a customer access token in PubNub.

## Endpoint

- **Method:** `POST`
- **Path:** `/oem/access-token`
- **Base URL:** `https://admin-api.pubnub.com/v2`
- **Official documentation:** [Issue Customer Access Token](https://www.pubnub.com/docs/admin-api/issue-customer-access-token)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | body | `number` | yes | PubNub application ID. |
| `customerUserId` | body | `string` | yes | Customer user identifier. |
| `expiresIn` | body | `string` | no | Optional token duration such as 1h. |
| `externalId` | body | `string` | yes | Customer external identifier. |
| `permissions[0]` | body | `string` | yes | First permission string. |
