# Rotate Secret Key with PubNub

Rotates a secret key for a PubNub keyset.

## Endpoint

- **Method:** `POST`
- **Path:** `/keysets/:keysetId/secret-keys`
- **Base URL:** `https://admin-api.pubnub.com/v2`
- **Official documentation:** [Rotate Secret Key](https://www.pubnub.com/docs/admin-api/rotate-secret-key)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keysetId` | path | `string` | yes | The PubNub keyset ID. |
