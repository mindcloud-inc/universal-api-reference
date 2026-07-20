# Update Secret Key Expiration Time with PubNub

Updates secret key expiration time in PubNub.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/keysets/:keysetId/secret-keys/:secretKeyPrefix`
- **Base URL:** `https://admin-api.pubnub.com/v2`
- **Official documentation:** [Update Secret Key Expiration Time](https://www.pubnub.com/docs/admin-api/update-secret-key-expiration-time)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keysetId` | path | `string` | yes | The PubNub keyset ID. |
| `secretKeyPrefix` | path | `string` | yes | The rotated secret key prefix in sec-c-xxxxx format. |
| `expiresAt` | body | `date` | yes | The new expiration time for the rotated secret key. |
