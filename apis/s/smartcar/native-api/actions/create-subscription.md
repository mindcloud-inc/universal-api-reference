# Create Subscription with Smartcar

Creates a new subscription in Smartcar.

## Endpoint

- **Method:** `POST`
- **Path:** `https://management.api.smartcar.com/v3/subscriptions`
- **Base URL:** `https://vehicle.api.smartcar.com/v3`
- **API:** rest
- **Official documentation:** [Create Subscription](https://smartcar.com/docs/api-reference/create-subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.attributes.userId` | body | `string` | yes | The Smartcar user ID tied to the subscription. |
| `data.attributes.vehicleId` | body | `string` | yes | The vehicle ID tied to the subscription. |
| `data.attributes.webhookId` | body | `string` | yes | The webhook that should receive the subscription. |
