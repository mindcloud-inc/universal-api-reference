# Create Order with Brightpearl

## Endpoint

- **Method:** `POST`
- **Path:** `/order-service/order/`
- **Base URL:** `https://{apiDomain}/public-api/{account}`
- **Official documentation:** [Create Order](https://api-docs.brightpearl.com/order/order/post.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderTypeCode` | body | `list<string>` | yes | Accepted values: `PC`, `PO`, `SC`, `SO`. |
| `reference` | body | `string` | no | — |
| `parentOrderId` | body | `string` | no | — |
| `priceListId` | body | `number` | no | — |
| `costPriceListId` | body | `number` | no | — |
| `priceModeCode` | body | `list<string>` | no | Applies to sales orders and sales credits. Accepted values: `EXC`, `INC`. |
| `placedOn` | body | `date` | no | — |
| `orderStatus` | body | `object` | no | — |
| `orderStatus.orderStatusId` | body | `number` | no | — |
| `delivery` | body | `object` | no | — |
| `delivery.deliveryDate` | body | `date` | no | — |
| `delivery.shippingMethodId` | body | `number` | no | — |
| `invoices[]` | body | `array<object>` | no | — |
| `invoices[].taxDate` | body | `date` | no | — |
| `currency` | body | `object` | no | — |
| `currency.orderCurrencyCode` | body | `string` | no | — |
| `currency.fixedExchangeRate` | body | `boolean` | no | — |
| `currency.exchangeRate` | body | `string` | no | Up to six decimal places. Requires fixed exchange rate. |
| `parties` | body | `object` | no | — |
| `parties.customer` | body | `object` | no | — |
| `parties.customer.contactId` | body | `number` | no | Required for sales orders (SO) and sales credits (SC). |
| `parties.supplier` | body | `object` | no | — |
| `parties.supplier.contactId` | body | `number` | no | Required for purchase orders (PO) and purchase credits (PC). |
| `parties.delivery` | body | `object` | no | — |
| `parties.delivery.addressFullName` | body | `string` | no | — |
| `parties.delivery.companyName` | body | `string` | no | — |
| `parties.delivery.addressLine1` | body | `string` | no | — |
| `parties.delivery.addressLine2` | body | `string` | no | — |
| `parties.delivery.addressLine3` | body | `string` | no | — |
| `parties.delivery.addressLine4` | body | `string` | no | — |
| `parties.delivery.postalCode` | body | `string` | no | — |
| `parties.delivery.countryId` | body | `string` | no | When providing a delivery address, supply country ID or country ISO code. |
| `parties.delivery.countryIsoCode` | body | `string` | no | When providing a delivery address, supply country ID or country ISO code. |
| `parties.delivery.telephone` | body | `string` | no | — |
| `parties.delivery.mobileTelephone` | body | `string` | no | — |
| `parties.delivery.fax` | body | `string` | no | — |
| `parties.delivery.email` | body | `string` | no | — |
| `assignment` | body | `object` | no | — |
| `assignment.current` | body | `object` | no | — |
| `assignment.current.channelId` | body | `number` | no | — |
| `assignment.current.leadSourceId` | body | `number` | no | — |
| `assignment.current.projectId` | body | `number` | no | — |
| `assignment.current.staffOwnerContactId` | body | `number` | no | — |
| `assignment.current.teamId` | body | `number` | no | — |
| `warehouseId` | body | `number` | no | — |
