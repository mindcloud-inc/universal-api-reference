# List Keysets For Customer with PubNub

Retrieves keysets for a PubNub customer.

## Endpoint

- **Method:** `GET`
- **Path:** `/oem/customers/:customerId/keysets`
- **Base URL:** `https://admin-api.pubnub.com/v2`
- **Official documentation:** [List Keysets For Customer](https://www.pubnub.com/docs/admin-api/list-keysets-for-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | query | `string` | no | Optional application filter. |
| `customerId` | path | `string` | no | PubNub customer ID. |
