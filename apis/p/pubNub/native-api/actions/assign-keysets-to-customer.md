# Assign Keysets To Customer with PubNub

Assigns keysets to a PubNub customer.

## Endpoint

- **Method:** `POST`
- **Path:** `/oem/customers/:customerId/keysets`
- **Base URL:** `https://admin-api.pubnub.com/v2`
- **Official documentation:** [Assign Keysets To Customer](https://www.pubnub.com/docs/admin-api/assign-keysets-to-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | no | PubNub customer ID. |
| `keysetIds[0]` | body | `number` | yes | First keyset ID to assign. |
