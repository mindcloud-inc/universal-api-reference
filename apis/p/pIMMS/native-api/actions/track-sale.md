# Track Sale with PIMMS

Creates a new tracked sale event in PIMMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/track/sale`
- **Base URL:** `https://api.pimms.io`
- **Official documentation:** [Track Sale](https://pimms.apidocumentation.com/reference#tag/track/POST/track/sale)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `externalId` | body | `string` | no | This is the unique identifier for the customer in the client's app. This is used to track the customer's journey. |
| `amount` | body | `number` | yes | The amount of the sale. Should be passed in cents. |
| `paymentProcessor` | body | `string` | yes | The payment processor via which the sale was made. |
| `eventName` | body | `string` | no | The name of the sale event. It can be used to track different types of event for example 'Purchase', 'Upgrade', 'Payment', etc. |
| `invoiceId` | body | `string` | no | The invoice ID of the sale. |
| `currency` | body | `string` | no | The currency of the sale. Accepts ISO 4217 currency codes. |
| `metadata` | body | `object` | no | Additional metadata to be stored with the sale event. |
