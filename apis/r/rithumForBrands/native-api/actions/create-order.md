# Create Order with Rithum for Brands

## Endpoint

- **Method:** `POST`
- **Path:** `Orders/Create`
- **Base URL:** `https://api.channeladvisor.com/v1/`
- **Official documentation:** [Create Order](https://knowledge.channeladvisor.com/kc?id=kb_article_view&sys_id=ae5173583304e290ae51a5373e5c7b5f&spa=1#concept-1655__section-49793)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `Items[].Sku` | body | `string` | yes |
| `ProfileID` | body | `list<number>` | yes |
| `Items[].UnitPrice` | body | `number` | yes |
| `SiteName` | body | `list` | yes |
| `Items[].Quantity` | body | `number` | yes |
| `SiteOrderID` | body | `string` | no |
| `Items[].TaxPrice` | body | `number` | no |
| `TotalPrice` | body | `number` | yes |
| `Items[].ShippingPrice` | body | `number` | no |
| `TotalTaxPrice` | body | `number` | no |
| `Items[].ShippingTaxPrice` | body | `number` | no |
| `TotalShippingPrice` | body | `number` | yes |
| `TotalShippingTaxPrice` | body | `number` | no |
| `EstimatedShipDateUtc` | body | `date` | no |
| `CheckoutStatus` | body | `list` | no |
| `PaymentStatus` | body | `list` | no |
| `ShippingStatus` | body | `list` | no |
| `BuyerUserId` | body | `string` | no |
| `BuyerEmailAddress` | body | `string` | yes |
| `PaymentMethod` | body | `string` | no |
| `PaymentCreditCardLast4` | body | `string` | no |
| `PaymentMerchantReferenceNumber` | body | `string` | no |
| `ShippingTitle` | body | `string` | no |
| `ShippingFirstName` | body | `string` | no |
| `ShippingLastName` | body | `string` | no |
| `ShippingSuffix` | body | `string` | no |
| `ShippingCompanyName` | body | `string` | no |
| `ShippingCompanyJobTitle` | body | `string` | no |
| `ShippingDaytimePhone` | body | `string` | no |
| `ShippingEveningPhone` | body | `string` | no |
| `CreatedDateUtc` | body | `date` | no |
| `ShippingAddressLine1` | body | `string` | no |
| `ShippingAddressLine2` | body | `string` | no |
| `ShippingCity` | body | `string` | no |
| `ShippingStateOrProvince` | body | `string` | no |
| `ShippingPostalCode` | body | `string` | no |
| `ShippingCountry` | body | `string` | no |
| `BillingTitle` | body | `string` | no |
| `BillingFirstName` | body | `string` | no |
| `BillingLastName` | body | `string` | no |
| `BillingSuffix` | body | `string` | no |
| `BillingCompanyName` | body | `string` | no |
| `BillingCompanyJobTitle` | body | `string` | no |
| `BillingDaytimePhone` | body | `string` | no |
| `BillingEveningPhone` | body | `string` | no |
| `BillingAddressLine1` | body | `string` | no |
| `BillingAddressLine2` | body | `string` | no |
| `BillingCity` | body | `string` | no |
| `BillingStateOrProvince` | body | `string` | no |
| `BillingPostalCode` | body | `string` | no |
| `BillingCountry` | body | `string` | no |
| `Items[]` | body | `array` | no |
