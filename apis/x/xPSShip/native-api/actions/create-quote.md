# Create Quote with XPS Ship

Creates a shipping quote in XPS Ship.

## Endpoint

- **Method:** `POST`
- **Path:** `/restapi/v1/customers/:customerId/quote`
- **Base URL:** `https://xpsshipper.com`
- **Official documentation:** [Create Quote](https://xpsshipper.com/restapi/docs/v1-ecommerce/endpoints/quote/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sender.country` | body | `string` | yes | ISO two-character sender country code. |
| `sender.zip` | body | `string` | yes | Sender ZIP or postal code. |
| `receiver.country` | body | `string` | yes | ISO two-character receiver country code. |
| `receiver.zip` | body | `string` | yes | Receiver ZIP or postal code. |
| `weightUnit` | body | `string` | yes | Weight unit: lb, oz, kg, or g. |
| `dimUnit` | body | `string` | yes | Dimension unit: in, cm, or null when package type has preset dimensions. |
| `currency` | body | `string` | yes | Currency for insurance, declared value, and customs value. |
| `customsCurrency` | body | `string` | yes | Currency for customs value. |
| `pieces` | body | `list<object>` | yes | Shipment pieces with weight, dimensions, insurance amount, and declared value. Send multiple values as a array. |
| `carrierCode` | body | `string` | no | Optional carrier code to limit the quote request. |
| `serviceCode` | body | `string` | no | Optional service code for quoting a specific service. |
| `packageTypeCode` | body | `string` | no | Optional package type code for quoting a specific package type. |
| `receiver.city` | body | `string` | no | Optional destination city or town. |
| `receiver.email` | body | `string` | no | Optional receiver email address. |
| `residential` | body | `boolean` | no | Set true when the destination address is residential. |
| `signatureOptionCode` | body | `string` | no | Optional signature option code for the shipment. |
| `uspsExpressAmDelivery` | body | `boolean` | no | Optional USPS 10:30 AM delivery flag. |
| `saturdayDelivery` | body | `boolean` | no | Optional Saturday delivery flag. |
| `contentType` | body | `string` | no | Optional carrier-specific content type. |
| `contentDescription` | body | `string` | no | Optional shipment content description, often needed for international shipments. |
| `billing.party` | body | `string` | no | Optional billing party: sender, receiver, or third_party. |
| `providerAccountId` | body | `string` | no | Optional provider account ID for the quote request. |
