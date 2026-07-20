# Subscribe To SMS Notifications with WeSupply

Subscribes a customer to WeSupply SMS notifications.

## Endpoint

- **Method:** `GET`
- **Path:** `/phone/v2/enrol`
- **Base URL:** `https://{subdomain}.labs.wesupply.xyz/api`
- **Official documentation:** [Subscribe To SMS Notifications](https://documenter.getpostman.com/view/11859344/T17AiAYq#706fe420-d329-47ca-a056-e5400a52dcad)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CustomerCountryCode` | query | `string` | no | The ISO country code for the customer. |
| `CustomerPhone` | query | `string` | no | The customer phone number to subscribe. |
| `CustomerPhonePrefix` | query | `string` | no | The international dialing prefix for the customer phone number. |
| `OrderExternalOrderID` | query | `string` | no | The external order ID to subscribe for SMS updates. |
