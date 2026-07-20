# Create Webhook with ChargeDesk

Creates a new webhook in ChargeDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://api.chargedesk.com/v1`
- **Official documentation:** [Create Webhook](https://chargedesk.com/api-docs#webhooks-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Webhook endpoint URL that ChargeDesk should send notifications to. |
| `all` | body | `number` | no | Set to 1 to subscribe this webhook to all available notification types. |
