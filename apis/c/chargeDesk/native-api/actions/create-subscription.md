# Create Subscription with ChargeDesk

Creates a new subscription in ChargeDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscriptions`
- **Base URL:** `https://api.chargedesk.com/v1`
- **Official documentation:** [Create Subscription](https://chargedesk.com/api-docs#subscriptions-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscription_id` | body | `string` | yes | Unique subscription identifier used to identify recurring charges. |
