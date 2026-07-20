# Create Keyset with PubNub

Creates a keyset in PubNub.

## Endpoint

- **Method:** `POST`
- **Path:** `/keysets`
- **Base URL:** `https://admin-api.pubnub.com/v2`
- **Official documentation:** [Create Keyset](https://www.pubnub.com/docs/admin-api/create-a-new-keyset)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keyset.appId` | body | `string` | yes | The PubNub app ID that will own the keyset. |
| `keyset.name` | body | `string` | yes | The PubNub keyset name. |
