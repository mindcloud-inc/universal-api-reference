# List Orders with Shopify

Retrieves orders from Shopify with GraphQL.

## Endpoint

- **Method:** `POST`
- **Path:** `2025-01/graphql.json`
- **Base URL:** `https://{storeName}.myshopify.com/admin/api/`
- **API:** REST
- **Official documentation:** [List Orders](https://shopify.dev/docs/api/admin-graphql/latest/queries/orders)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `createdAt` | body | `string` | no | Date created after |
| `updatedAt` | body | `string` | no | Date updated after |
| `updatedBefore` | body | `string` | no | — |
| `financialStatus` | body | `list` | no | — |
| `fulfillmentStatus` | body | `list<string>` | no | — |
| `email` | body | `string` | no | — |
| `ids[]` | body | `array<string>` | no | — |
| `names[]` | body | `array<string>` | no | — |
| `customQuery` | body | `string` | no | Optional Shopify order search query to combine with the built-in filters. |
| `reverse` | body | `boolean` | no | Reverse the sort order of the results Format: `toggle`. |
| `simple` | body | `boolean` | no | Return a lighter order payload when you only need core order fields. Leave OFF if you need only specific advanced fields Format: `toggle`. |
| `purchasingEntity` | body | `boolean` | no | Adds field: purchasingEntity Format: `toggle`. |
| `totalPriceSet` | body | `boolean` | no | Adds field: totalPriceSet Format: `toggle`. |
| `currentCartDiscountAmountSet` | body | `boolean` | no | Adds field: currentCartDiscountAmountSet Format: `toggle`. |
| `currentTotalDiscountsSet` | body | `boolean` | no | Adds field: currentTotalDiscountsSet Format: `toggle`. |
| `currentTotalTaxSet` | body | `boolean` | no | Adds field: currentTotalTaxSet Format: `toggle`. |
| `totalTaxSet` | body | `boolean` | no | Adds field: totalTaxSet Format: `toggle`. |
| `currentTaxLines` | body | `boolean` | no | Adds field: currentTaxLines Format: `toggle`. |
| `taxLine` | body | `boolean` | no | Adds field: taxLine Format: `toggle`. |
| `fulfillmentOrders` | body | `boolean` | no | Adds field: fulfillmentOrders Format: `toggle`. |
| `totalShippingPriceSet` | body | `boolean` | no | Adds field: totalShippingPriceSet Format: `toggle`. |
| `shippingLine` | body | `boolean` | no | Adds field: shippingLine Format: `toggle`. |
| `shippingLines` | body | `boolean` | no | Adds field: shippingLines Format: `toggle`. |
| `billingAddress` | body | `boolean` | no | Adds field: billingAddress Format: `toggle`. |
| `netPaymentSet` | body | `boolean` | no | Adds field: netPaymentSet Format: `toggle`. |
| `customer` | body | `boolean` | no | Adds field: customer Format: `toggle`. |
| `paymentGatewayNames` | body | `boolean` | no | Adds field: paymentGatewayNames Format: `toggle`. |
| `retailLocation` | body | `boolean` | no | Adds field: retailLocation Format: `toggle`. |
| `transactions` | body | `boolean` | no | Adds field: transactions Format: `toggle`. |
| `metafields` | body | `boolean` | no | Adds field: metafields Format: `toggle`. |
| `test` | body | `boolean` | no | Adds field: test Format: `toggle`. |
| `advancedLineItems` | body | `boolean` | no | Adds metafields to Line Items Format: `toggle`. |
