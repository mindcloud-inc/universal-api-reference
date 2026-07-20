# Delete Rotated Secret Key with PubNub

Deletes a rotated secret key from PubNub.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/keysets/:keysetId/secret-keys/:secretKeyPrefix`
- **Base URL:** `https://admin-api.pubnub.com/v2`
- **Official documentation:** [Delete Rotated Secret Key](https://www.pubnub.com/docs/admin-api/delete-a-rotated-secret-key)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keysetId` | path | `string` | yes | The PubNub keyset ID. |
| `secretKeyPrefix` | path | `string` | yes | The rotated secret key prefix in sec-c-xxxxx format. |
