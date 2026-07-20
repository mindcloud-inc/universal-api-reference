# Create Customer with PubNub

Creates a customer in PubNub.

## Endpoint

- **Method:** `POST`
- **Path:** `/oem/customers`
- **Base URL:** `https://admin-api.pubnub.com/v2`
- **Official documentation:** [Create Customer](https://www.pubnub.com/docs/admin-api/create-a-new-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `externalId` | body | `string` | no | Your unique tenant or customer identifier. |
| `name` | body | `string` | no | Customer display name. |
