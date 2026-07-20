# Unsubscribe From SMS Notifications with WeSupply

Unsubscribes a customer from WeSupply SMS notifications.

## Endpoint

- **Method:** `GET`
- **Path:** `/phone/v2/unsubscribe`
- **Base URL:** `https://{subdomain}.labs.wesupply.xyz/api`
- **Official documentation:** [Unsubscribe From SMS Notifications](https://documenter.getpostman.com/view/11859344/T17AiAYq#e0f3c127-f724-4db2-a686-c09937b76a3a)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CustomerPhone` | query | `string` | no | The customer phone number to unsubscribe. |
| `OrderExternalOrderID` | query | `string` | no | The external order ID to unsubscribe from SMS updates. |
