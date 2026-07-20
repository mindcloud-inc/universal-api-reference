# Create Order with SquareSpace

Creates an order in Squarespace.

## Endpoint

- **Method:** `POST`
- **Path:** `/1.0/commerce/orders`
- **Base URL:** `https://api.squarespace.com`
- **Official documentation:** [Create Order](https://developers.squarespace.com/commerce-apis/orders#create-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelName` | body | `string` | yes | Sales channel name for the order. |
| `createdOn` | body | `date` | yes | Order creation datetime in ISO 8601 UTC format. |
| `customerEmail` | body | `string` | no | Customer email address. |
| `externalOrderReference` | body | `string` | yes | External system order reference. |
| `grandTotal.currency` | body | `string` | yes | ISO 4217 currency code for order grand total. |
| `grandTotal.value` | body | `string` | yes | Monetary amount for order grand total. |
| `idempotencyKey` | query | `string` | yes | Unique idempotency key for safe create-order retries. |
| `lineItems[]` | body | `array<object>` | yes | Order line items. |
| `lineItems[].lineItemType` | body | `list<string>` | yes | Product type sold for each line item. Accepted values: `CUSTOM`, `PHYSICAL_PRODUCT`. |
| `lineItems[].quantity` | body | `number` | yes | Quantity for line item. |
| `lineItems[].unitPricePaid.currency` | body | `string` | yes | ISO 4217 currency code for line item unit price. |
| `lineItems[].unitPricePaid.value` | body | `string` | yes | Monetary amount for line item unit price. |
| `lineItems[].variantId` | body | `list<string>` | yes | Variant ID for line item. |
| `priceTaxInterpretation` | body | `list<string>` | yes | Whether item prices include or exclude tax. Accepted values: `EXCLUSIVE`, `INCLUSIVE`. |
| `subtotal.currency` | body | `string` | yes | ISO 4217 currency code for order subtotal. |
| `subtotal.value` | body | `string` | yes | Monetary amount for order subtotal. |
