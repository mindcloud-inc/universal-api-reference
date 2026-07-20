# Update Keyset Configuration with PubNub

Updates keyset configuration in PubNub.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/keysets/:id/config`
- **Base URL:** `https://admin-api.pubnub.com/v2`
- **Official documentation:** [Update Keyset Configuration](https://www.pubnub.com/docs/admin-api/update-keyset-configuration)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The PubNub keyset ID. |
| `presence.enabled` | body | `boolean` | yes | Whether presence is enabled for the keyset. |
