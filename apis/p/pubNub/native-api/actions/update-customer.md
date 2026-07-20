# Update Customer with PubNub

Updates an existing customer in PubNub.

## Endpoint

- **Method:** `PUT`
- **Path:** `/oem/customers/:customerId`
- **Base URL:** `https://admin-api.pubnub.com/v2`
- **Official documentation:** [Update Customer](https://www.pubnub.com/docs/admin-api/update-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `string` | no | PubNub customer ID. |
| `name` | body | `string` | no | Updated customer display name. |
