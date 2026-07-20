# List Secret Keys For Keyset with PubNub

Retrieves secret keys for a PubNub keyset.

## Endpoint

- **Method:** `GET`
- **Path:** `/keysets/:keysetId/secret-keys`
- **Base URL:** `https://admin-api.pubnub.com/v2`
- **Official documentation:** [List Secret Keys For Keyset](https://www.pubnub.com/docs/admin-api/list-secret-keys-for-a-keyset)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keysetId` | path | `string` | yes | The PubNub keyset ID. |
