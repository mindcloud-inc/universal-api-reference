# Create Sales Offer with Merit

## Endpoint

- **Method:** `POST`
- **Path:** `v2/sendoffer`
- **Base URL:** `https://aktiva.merit.ee/api`
- **Official documentation:** [Create Sales Offer](https://api.merit.ee/connecting-robots/reference-manual/sales-offers/create-sales-offer/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Customer` | body | `object` | yes | Customer object, for example {"Id":"..."}. |
| `DocDate` | body | `string` | yes | Offer date in Merit date string format. |
| `ExpireDate` | body | `string` | yes | Offer expiry date in Merit date string format. |
| `OfferNo` | body | `string` | yes | Sales offer number. |
| `DocType` | body | `number` | no | Sales offer type code. |
| `OfferRow[]` | body | `array<object>` | yes | Array of offer row objects. |
| `TaxAmount[]` | body | `array<object>` | yes | Array of tax amount objects. |
| `TotalAmount` | body | `number` | yes | Offer total amount. |
| `CurrencyCode` | body | `string` | no | Currency code, for example EUR. |
