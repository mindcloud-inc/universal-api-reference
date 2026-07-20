# Create Quote with Ascora

Creates a new quote in Ascora.

## Endpoint

- **Method:** `POST`
- **Path:** `/Quotes/Quote`
- **Base URL:** `https://api.ascora.com.au`
- **Official documentation:** [Create Quote](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=27)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `siteCustomer.id` | body | `string` | no |
| `billingCustomer.id` | body | `string` | no |
| `quoteName` | body | `string` | no |
| `quoteDescription` | body | `string` | no |
| `quotationDate` | body | `string` | no |
| `pricingMethod` | body | `string` | no |
| `purchaseOrderNumber` | body | `string` | no |
| `clientOrderNumber` | body | `string` | no |
| `addressLine1` | body | `string` | no |
| `addressLine2` | body | `string` | no |
| `suburb` | body | `string` | no |
| `postcode` | body | `string` | no |
| `country` | body | `string` | no |
