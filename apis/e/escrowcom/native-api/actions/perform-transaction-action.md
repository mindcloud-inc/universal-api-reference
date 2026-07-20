# Perform Transaction Action with Escrow.com

Performs a transaction action in Escrow.com.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/transaction/:transaction_id`
- **Base URL:** `https://api.escrow-sandbox.com/2017-09-01`
- **Official documentation:** [Perform Transaction Action](https://www.escrow.com/api/docs/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transaction_id` | path | `number` | yes | The Escrow.com transaction ID. |
| `action` | body | `string` | yes | Transaction action to perform, such as agree, ship, receive, accept, reject, cancel, or return. |
| `action_to` | body | `string` | no | Party role the action is performed for, such as buyer or seller, when supported. |
| `as_customer` | query | `string` | no | Escrow.com customer email to send as the As-Customer header when acting as a partner on behalf of a party. |
