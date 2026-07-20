# Get Milestone Item Web URL with Escrow.com

Retrieves a milestone item web URL from Escrow.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/transaction/:transaction_id/item/:item_id/web_link/:action`
- **Base URL:** `https://api.escrow-sandbox.com/2017-09-01`
- **Official documentation:** [Get Milestone Item Web URL](https://www.escrow.com/api/docs/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transaction_id` | path | `number` | yes | The Escrow.com transaction ID. |
| `item_id` | path | `number` | yes | The milestone item ID. |
| `action` | path | `string` | yes | Web action to perform on this milestone item. |
| `as_customer` | query | `string` | no | Escrow.com customer email to send as the As-Customer header when acting as a partner on behalf of a party. |
