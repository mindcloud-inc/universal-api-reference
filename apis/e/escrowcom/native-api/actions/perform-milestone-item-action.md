# Perform Milestone Item Action with Escrow.com

Performs a milestone item action in Escrow.com.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/transaction/:transaction_id/item/:item_id`
- **Base URL:** `https://api.escrow-sandbox.com/2017-09-01`
- **Official documentation:** [Perform Milestone Item Action](https://www.escrow.com/api/docs/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transaction_id` | path | `number` | yes | The Escrow.com transaction ID. |
| `item_id` | path | `number` | yes | The milestone item ID. |
| `action` | body | `string` | yes | Milestone item action to perform. |
| `as_customer` | query | `string` | no | Escrow.com customer email to send as the As-Customer header when acting as a partner on behalf of a party. |
