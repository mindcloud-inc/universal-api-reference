# Update Keyset with PubNub

Updates an existing keyset in PubNub.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/keysets/:id`
- **Base URL:** `https://admin-api.pubnub.com/v2`
- **Official documentation:** [Update Keyset](https://www.pubnub.com/docs/admin-api/update-keyset-name-and-or-type)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The PubNub keyset ID. |
| `name` | body | `string` | yes | The updated PubNub keyset name. |
